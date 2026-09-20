---
name: 2s-io-watchers-and-callbacks
description: Arm a 2s watcher or schedule, receive its EIP-191-signed HTTP callback, recover missed pushes from the status endpoint, and cancel it — with the payment, window and idempotency rules the contract states.
api: openapi/2s-io-openapi.json
operations:
  - watchers_crypto-address-activity
  - watchers_stock-price
  - watchers_sec-filing
  - watchers_status
  - watchers_cancel
  - schedule_create
  - schedule_status
  - schedule_cancel
  - pubsub_create-topic
  - pubsub_subscribe
  - pubsub_publish
  - pubsub_unsubscribe
method: generated
generated: '2026-09-19'
grounding: Every operationId above exists verbatim in openapi/2s-io-openapi.json (live https://2s.io/openapi.json, 2026-09-19); prices, windows and limits are quoted from those operations' descriptions and requestBody schemas, and from https://2s.io/llms.txt.
---

# Get woken up instead of polling

2s's watchers, schedules and pub/sub are the write side of an otherwise read-heavy catalog: you pay once to arm something, and 2s POSTs to your `callbackUrl` when it fires. Every push is EIP-191-signed by the provider's published key and retried with exponential backoff. Nothing here needs an account or API key — the paying wallet (the x402 payer) is the tenant, and everything you arm is private to it.

## 0. Pay like every other 2s call

Call the endpoint with no auth; read the `402` envelope (`accepts[]` lists Base USDC and Solana USDC with the price in `accepts[].amount`); sign for the rail you hold (EIP-3009 `transferWithAuthorization` on Base, partial SPL transfer on Solana); retry with the base64 payload in `PAYMENT-SIGNATURE`. A `200` carries `X-PAYMENT-TX`. The SDKs (`@2sio/sdk`, `2sio`) and the MCP server do this loop for you. `?trial=1` gives one free real call per endpoint per hour, which is enough to see a watcher arm.

## 1. Arm a watcher (27 kinds, flat $0.125 each)

- `POST /api/watchers/crypto-address-activity` (`watchers_crypto-address-activity`) — body `chain` (base | ethereum | bitcoin), `address`, `callbackUrl`, optional `direction` (in | out | both), `assetTypes` (native | erc20 | erc721), `minValueUsd`, `payload` (arbitrary JSON echoed back verbatim in every callback), `expiresInSeconds` (default 2592000 = 30 days), `maxFires` (default 25, max 1000), `label`.
- `POST /api/watchers/stock-price` (`watchers_stock-price`) — fires when a US stock crosses a price or % move.
- `POST /api/watchers/sec-filing` (`watchers_sec-filing`) — fires on each new EDGAR filing for a company.

Each returns a `watcherId`. The watch ends at whichever comes first: `expiresInSeconds` or `maxFires`. Per the contract this is a flat-fee model — there is nothing held or owed after arming.

## 2. Verify the callback

The JSON body 2s POSTs to `callbackUrl` includes your `payload`; the request is EIP-191-signed by the provider's published key, so verify offline before acting. The provider's published signer for response attestation is `0xC20d180f1d8aaf2117d13252C5E803895F0D7717` (`https://2s.io/.well-known/2s-attestation.json`); the watcher callback signature header is described in the spec as `X-2s-Signature`. Treat any callback that fails verification as noise.

## 3. Never lose a fire — the pull backstop

`GET /api/watchers/status?watcherId=…` (`watchers_status`) returns `state` (armed | completed | expired | cancelled), fires used/remaining, expiry, recent deliveries with HTTP result and attempt count, and any UNDELIVERED events with their full callback bodies. If your endpoint was down, read them here rather than re-arming.

## 4. Cancel

`POST /api/watchers/cancel` (`watchers_cancel`) with `watcherId` stops the watch immediately. The contract states it is idempotent and that there is no refund of the unused window. This is the only reversal path for a watcher — the arming payment itself is not reversible.

## 5. Time-driven instead of event-driven

`POST /api/schedule/create` (`schedule_create`, $0.125) — `callbackUrl` plus either `at` (ISO-8601, one shot) or `everySeconds` (≥ 60, recurring); `maxFires` (default 25, max 1000) and `expiresInSeconds` (default and max 90 days). Callback bodies carry your `payload` plus `scheduleId`, `fireNumber`, `firedAt`. Check with `POST /api/schedule/status` (`schedule_status`); stop with `POST /api/schedule/cancel` (`schedule_cancel`) — "No more callbacks will fire. Returns cancelled:false if it was already done/cancelled or isn't yours. No refund of the unused window."

## 6. Fan-out to other agents

`POST /api/pubsub/create-topic` (`pubsub_create-topic`, idempotent per the contract) → `topicId`. Subscribers call `POST /api/pubsub/subscribe` (`pubsub_subscribe`, $0.005) with `topicId` and `callbackUrl`; 2s immediately POSTs a one-time challenge carrying `X-2s-Confirmation-Token` and `{type: "2s_subscription_confirmation", token}`, and the endpoint must answer 2xx with exactly that token (or `{"token": …}`) to be confirmed — unconfirmed URLs never receive messages. Up to 100 subscribers per topic, one per URL; a subscriber that repeatedly fails delivery is auto-disabled. The owner publishes with `POST /api/pubsub/publish` (`pubsub_publish`); a subscriber leaves with `POST /api/pubsub/unsubscribe` (`pubsub_unsubscribe`) using its `subscriptionId`.

## Rules that bite

- 429 with code `RATE_LIMITED` is 2s's own limiter — back off. 503 `UPSTREAM_RATE_LIMIT` is an upstream throttle — the provider says retry without client-side backoff (changelog 1.80.1).
- Errors arrive as `{"error": {"code", "message", "details"}}`; 400 `BAD_REQUEST` carries a Zod-style `details.issues[]` naming the offending field.
- A failed handler is never charged on-chain (status page commitment); a `200` is what you paid for.
- Wallet-scoped state (store, locks, queues) shares one tenant quota: 50 MB storage, 1,000 queue depth, 100 concurrent locks (changelog 1.80.0).
