# 2s

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

2s ("the (most) everything API", 2s.io) is a pay-per-call REST API built for AI agents: 575 endpoints across 112 groups on one origin — US public records and government data, company and legal identifiers (GLEIF, OFAC, state registries), SEC filings, crypto and web3, security and CVEs, patents and case law, medical codes, weather and geocoding, ANSI X12 / EDIFACT EDI, an OpenAI-compatible AI gateway (chat, image, multi-model council) and wallet-scoped agent infrastructure (kv/doc/vector/blob store, locks, queues, schedules, pub/sub and 26 kinds of signed-callback watchers). There are no accounts and no API keys: every call is paid in USDC on Base or Solana through the x402 protocol (HTTP 402 → sign → retry), with a free trial call per endpoint per hour and actual-usage "upto" billing on AI endpoints. The same catalog is published as an OpenAPI 3.1.0 contract at https://2s.io/openapi.json, a remote MCP server at https://2s.io/mcp (plus the npx @2sio/mcp local server), an A2A 0.3.0 agent card whose one skill is endpoint discovery, an RFC 9727 API catalog, an APIs.json index, an llms.txt, an MCP server card, an x402 manifest and an ERC-8004 on-chain agent registration. Maintained by an individual operator (alley@2s.io); the SDK monorepo is github.com/2s-io/sdk.

**Areas:** Agents · Agentic Commerce · x402 · MCP · A2A · Public Records · Government Data · Finance · Cryptocurrency · Security · Legal · Weather

## 2s on APIs.io

Everything profiled for 2s is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/2s-io/](https://apis.io/providers/2s-io/)** — or go straight to one of the APIs or properties below.

### APIs (114)

- [2s MCP Server](https://apis.io/apis/2s-io/2s-mcp-server/) — Remote Model Context Protocol server at https://2s.io/mcp (Streamable HTTP, POST only, protocol version 2025-06-18, serverInfo 2s.io 1.0.0). initialize and…
- [2s A2A Agent](https://apis.io/apis/2s-io/2s-a2a-agent/) — Agent2Agent (A2A) protocol surface: an agent card served from https://2s.io/.well-known/agent-card.json (protocolVersion 0.3.0, JSONRPC transport, version…
- [2s Agent API](https://apis.io/apis/2s-io/2s-io-agent-api/) — The agent API from 2s — 1 operation(s) for agent.
- [2s Agriculture API](https://apis.io/apis/2s-io/2s-io-agriculture-api/) — The agriculture API from 2s — 2 operation(s) for agriculture.
- [2s AI API](https://apis.io/apis/2s-io/2s-io-ai-api/) — The ai API from 2s — 16 operation(s) for ai.
- [2s Airport API](https://apis.io/apis/2s-io/2s-io-airport-api/) — The airport API from 2s — 2 operation(s) for airport.
- [2s Aviation API](https://apis.io/apis/2s-io/2s-io-aviation-api/) — The aviation API from 2s — 4 operation(s) for aviation.
- [2s Bank API](https://apis.io/apis/2s-io/2s-io-bank-api/) — The bank API from 2s — 1 operation(s) for bank.
- [2s Barcode API](https://apis.io/apis/2s-io/2s-io-barcode-api/) — The barcode API from 2s — 1 operation(s) for barcode.
- [2s Batch API](https://apis.io/apis/2s-io/2s-io-batch-api/) — The batch API from 2s — 1 operation(s) for batch.
- [2s Bio API](https://apis.io/apis/2s-io/2s-io-bio-api/) — The bio API from 2s — 3 operation(s) for bio.
- [2s Bls API](https://apis.io/apis/2s-io/2s-io-bls-api/) — The bls API from 2s — 1 operation(s) for bls.
- [2s Book API](https://apis.io/apis/2s-io/2s-io-book-api/) — The book API from 2s — 1 operation(s) for book.
- [2s Business API](https://apis.io/apis/2s-io/2s-io-business-api/) — The business API from 2s — 16 operation(s) for business.
- [2s Calendar API](https://apis.io/apis/2s-io/2s-io-calendar-api/) — The calendar API from 2s — 4 operation(s) for calendar.
- [2s Census API](https://apis.io/apis/2s-io/2s-io-census-api/) — The census API from 2s — 2 operation(s) for census.
- [2s Chem API](https://apis.io/apis/2s-io/2s-io-chem-api/) — The chem API from 2s — 1 operation(s) for chem.
- [2s Chinese API](https://apis.io/apis/2s-io/2s-io-chinese-api/) — The chinese API from 2s — 3 operation(s) for chinese.
- [2s Class API](https://apis.io/apis/2s-io/2s-io-class-api/) — The class API from 2s — 1 operation(s) for class.
- [2s Climate API](https://apis.io/apis/2s-io/2s-io-climate-api/) — The climate API from 2s — 2 operation(s) for climate.
- [2s Clinical API](https://apis.io/apis/2s-io/2s-io-clinical-api/) — The clinical API from 2s — 2 operation(s) for clinical.
- [2s Code API](https://apis.io/apis/2s-io/2s-io-code-api/) — The code API from 2s — 1 operation(s) for code.
- [2s Convert API](https://apis.io/apis/2s-io/2s-io-convert-api/) — The convert API from 2s — 2 operation(s) for convert.
- [2s Countdown API](https://apis.io/apis/2s-io/2s-io-countdown-api/) — The countdown API from 2s — 1 operation(s) for countdown.
- [2s Country API](https://apis.io/apis/2s-io/2s-io-country-api/) — The country API from 2s — 2 operation(s) for country.
- [2s Crypto API](https://apis.io/apis/2s-io/2s-io-crypto-api/) — The crypto API from 2s — 46 operation(s) for crypto.
- [2s Dev API](https://apis.io/apis/2s-io/2s-io-dev-api/) — The dev API from 2s — 15 operation(s) for dev.
- [2s Dns API](https://apis.io/apis/2s-io/2s-io-dns-api/) — The dns API from 2s — 1 operation(s) for dns.
- [2s Domain API](https://apis.io/apis/2s-io/2s-io-domain-api/) — The domain API from 2s — 4 operation(s) for domain.
- [2s Earth API](https://apis.io/apis/2s-io/2s-io-earth-api/) — The earth API from 2s — 2 operation(s) for earth.
- [2s Econ API](https://apis.io/apis/2s-io/2s-io-econ-api/) — The econ API from 2s — 10 operation(s) for econ.
- [2s Edi API](https://apis.io/apis/2s-io/2s-io-edi-api/) — The edi API from 2s — 5 operation(s) for edi.
- [2s Edu API](https://apis.io/apis/2s-io/2s-io-edu-api/) — The edu API from 2s — 2 operation(s) for edu.
- [2s Email API](https://apis.io/apis/2s-io/2s-io-email-api/) — The email API from 2s — 1 operation(s) for email.
- [2s Energy API](https://apis.io/apis/2s-io/2s-io-energy-api/) — The energy API from 2s — 8 operation(s) for energy.
- [2s Factcheck API](https://apis.io/apis/2s-io/2s-io-factcheck-api/) — The factcheck API from 2s — 1 operation(s) for factcheck.
- [2s Feedback API](https://apis.io/apis/2s-io/2s-io-feedback-api/) — The feedback API from 2s — 1 operation(s) for feedback.
- [2s Finance API](https://apis.io/apis/2s-io/2s-io-finance-api/) — The finance API from 2s — 17 operation(s) for finance.
- [2s Flight API](https://apis.io/apis/2s-io/2s-io-flight-api/) — The flight API from 2s — 3 operation(s) for flight.
- [2s Food API](https://apis.io/apis/2s-io/2s-io-food-api/) — The food API from 2s — 2 operation(s) for food.
- [2s Fx API](https://apis.io/apis/2s-io/2s-io-fx-api/) — The fx API from 2s — 2 operation(s) for fx.
- [2s Geo API](https://apis.io/apis/2s-io/2s-io-geo-api/) — The geo API from 2s — 7 operation(s) for geo.
- [2s Geocode API](https://apis.io/apis/2s-io/2s-io-geocode-api/) — The geocode API from 2s — 2 operation(s) for geocode.
- [2s GitHub API](https://apis.io/apis/2s-io/2s-io-github-api/) — The github API from 2s — 14 operation(s) for github.
- [2s Gov API](https://apis.io/apis/2s-io/2s-io-gov-api/) — The gov API from 2s — 56 operation(s) for gov.
- [2s Hash API](https://apis.io/apis/2s-io/2s-io-hash-api/) — The hash API from 2s — 1 operation(s) for hash.
- [2s Health API](https://apis.io/apis/2s-io/2s-io-health-api/) — The health API from 2s — 7 operation(s) for health.
- [2s Html API](https://apis.io/apis/2s-io/2s-io-html-api/) — The html API from 2s — 1 operation(s) for html.
- [2s Image API](https://apis.io/apis/2s-io/2s-io-image-api/) — The image API from 2s — 1 operation(s) for image.
- [2s Inflation API](https://apis.io/apis/2s-io/2s-io-inflation-api/) — The inflation API from 2s — 4 operation(s) for inflation.
- [2s Ipinfo API](https://apis.io/apis/2s-io/2s-io-ipinfo-api/) — The ipinfo API from 2s — 1 operation(s) for ipinfo.
- [2s Iso API](https://apis.io/apis/2s-io/2s-io-iso-api/) — The iso API from 2s — 3 operation(s) for iso.
- [2s Job API](https://apis.io/apis/2s-io/2s-io-job-api/) — The job API from 2s — 2 operation(s) for job.
- [2s Labor API](https://apis.io/apis/2s-io/2s-io-labor-api/) — The labor API from 2s — 3 operation(s) for labor.
- [2s Law API](https://apis.io/apis/2s-io/2s-io-law-api/) — The law API from 2s — 12 operation(s) for law.
- [2s License API](https://apis.io/apis/2s-io/2s-io-license-api/) — The license API from 2s — 4 operation(s) for license.
- [2s Lock API](https://apis.io/apis/2s-io/2s-io-lock-api/) — The lock API from 2s — 3 operation(s) for lock.
- [2s Maritime API](https://apis.io/apis/2s-io/2s-io-maritime-api/) — The maritime API from 2s — 3 operation(s) for maritime.
- [2s Markets API](https://apis.io/apis/2s-io/2s-io-markets-api/) — The markets API from 2s — 2 operation(s) for markets.
- [2s Medical API](https://apis.io/apis/2s-io/2s-io-medical-api/) — The medical API from 2s — 14 operation(s) for medical.
- [2s Music API](https://apis.io/apis/2s-io/2s-io-music-api/) — The music API from 2s — 3 operation(s) for music.
- [2s Net API](https://apis.io/apis/2s-io/2s-io-net-api/) — The net API from 2s — 4 operation(s) for net.
- [2s News API](https://apis.io/apis/2s-io/2s-io-news-api/) — The news API from 2s — 5 operation(s) for news.
- [2s Nonprofit API](https://apis.io/apis/2s-io/2s-io-nonprofit-api/) — The nonprofit API from 2s — 2 operation(s) for nonprofit.
- [2s Nutrition API](https://apis.io/apis/2s-io/2s-io-nutrition-api/) — The nutrition API from 2s — 1 operation(s) for nutrition.
- [2s Occupation API](https://apis.io/apis/2s-io/2s-io-occupation-api/) — The occupation API from 2s — 3 operation(s) for occupation.
- [2s Paper API](https://apis.io/apis/2s-io/2s-io-paper-api/) — The paper API from 2s — 1 operation(s) for paper.
- [2s Papers API](https://apis.io/apis/2s-io/2s-io-papers-api/) — The papers API from 2s — 2 operation(s) for papers.
- [2s Park API](https://apis.io/apis/2s-io/2s-io-park-api/) — The park API from 2s — 1 operation(s) for park.
- [2s Patents API](https://apis.io/apis/2s-io/2s-io-patents-api/) — The patents API from 2s — 7 operation(s) for patents.
- [2s Person API](https://apis.io/apis/2s-io/2s-io-person-api/) — The person API from 2s — 1 operation(s) for person.
- [2s Phone API](https://apis.io/apis/2s-io/2s-io-phone-api/) — The phone API from 2s — 1 operation(s) for phone.
- [2s Poi API](https://apis.io/apis/2s-io/2s-io-poi-api/) — The poi API from 2s — 1 operation(s) for poi.
- [2s Predict API](https://apis.io/apis/2s-io/2s-io-predict-api/) — The predict API from 2s — 23 operation(s) for predict.
- [2s Product API](https://apis.io/apis/2s-io/2s-io-product-api/) — The product API from 2s — 1 operation(s) for product.
- [2s Property API](https://apis.io/apis/2s-io/2s-io-property-api/) — The property API from 2s — 4 operation(s) for property.
- [2s Pubsub API](https://apis.io/apis/2s-io/2s-io-pubsub-api/) — The pubsub API from 2s — 4 operation(s) for pubsub.
- [2s Quakes API](https://apis.io/apis/2s-io/2s-io-quakes-api/) — The quakes API from 2s — 1 operation(s) for quakes.
- [2s Queue API](https://apis.io/apis/2s-io/2s-io-queue-api/) — The queue API from 2s — 4 operation(s) for queue.
- [2s Recreation API](https://apis.io/apis/2s-io/2s-io-recreation-api/) — The recreation API from 2s — 1 operation(s) for recreation.
- [2s Registry API](https://apis.io/apis/2s-io/2s-io-registry-api/) — The registry API from 2s — 2 operation(s) for registry.
- [2s Research API](https://apis.io/apis/2s-io/2s-io-research-api/) — The research API from 2s — 3 operation(s) for research.
- [2s Schedule API](https://apis.io/apis/2s-io/2s-io-schedule-api/) — The schedule API from 2s — 3 operation(s) for schedule.
- [2s Search API](https://apis.io/apis/2s-io/2s-io-search-api/) — The search API from 2s — 5 operation(s) for search.
- [2s Security API](https://apis.io/apis/2s-io/2s-io-security-api/) — The security API from 2s — 16 operation(s) for security.
- [2s Soil API](https://apis.io/apis/2s-io/2s-io-soil-api/) — The soil API from 2s — 2 operation(s) for soil.
- [2s Space API](https://apis.io/apis/2s-io/2s-io-space-api/) — The space API from 2s — 11 operation(s) for space.
- [2s Sports API](https://apis.io/apis/2s-io/2s-io-sports-api/) — The sports API from 2s — 11 operation(s) for sports.
- [2s Stocks API](https://apis.io/apis/2s-io/2s-io-stocks-api/) — The stocks API from 2s — 14 operation(s) for stocks.
- [2s Store API](https://apis.io/apis/2s-io/2s-io-store-api/) — The store API from 2s — 16 operation(s) for store.
- [2s Sunrise API](https://apis.io/apis/2s-io/2s-io-sunrise-api/) — The sunrise API from 2s — 1 operation(s) for sunrise.
- [2s Tax API](https://apis.io/apis/2s-io/2s-io-tax-api/) — The tax API from 2s — 2 operation(s) for tax.
- [2s Tcg API](https://apis.io/apis/2s-io/2s-io-tcg-api/) — The tcg API from 2s — 4 operation(s) for tcg.
- [2s Telecom API](https://apis.io/apis/2s-io/2s-io-telecom-api/) — The telecom API from 2s — 2 operation(s) for telecom.
- [2s Text API](https://apis.io/apis/2s-io/2s-io-text-api/) — The text API from 2s — 1 operation(s) for text.
- [2s Tides API](https://apis.io/apis/2s-io/2s-io-tides-api/) — The tides API from 2s — 1 operation(s) for tides.
- [2s Time API](https://apis.io/apis/2s-io/2s-io-time-api/) — The time API from 2s — 1 operation(s) for time.
- [2s Timezone API](https://apis.io/apis/2s-io/2s-io-timezone-api/) — The timezone API from 2s — 1 operation(s) for timezone.
- [2s Tld API](https://apis.io/apis/2s-io/2s-io-tld-api/) — The tld API from 2s — 1 operation(s) for tld.
- [2s Tls API](https://apis.io/apis/2s-io/2s-io-tls-api/) — The tls API from 2s — 1 operation(s) for tls.
- [2s Trade API](https://apis.io/apis/2s-io/2s-io-trade-api/) — The trade API from 2s — 4 operation(s) for trade.
- [2s Transcribe API](https://apis.io/apis/2s-io/2s-io-transcribe-api/) — The transcribe API from 2s — 1 operation(s) for transcribe.
- [2s Travel API](https://apis.io/apis/2s-io/2s-io-travel-api/) — The travel API from 2s — 2 operation(s) for travel.
- [2s Treasury API](https://apis.io/apis/2s-io/2s-io-treasury-api/) — The treasury API from 2s — 4 operation(s) for treasury.
- [2s URL API](https://apis.io/apis/2s-io/2s-io-url-api/) — The url API from 2s — 4 operation(s) for url.
- [2s Validate API](https://apis.io/apis/2s-io/2s-io-validate-api/) — The validate API from 2s — 10 operation(s) for validate.
- [2s Vehicle API](https://apis.io/apis/2s-io/2s-io-vehicle-api/) — The vehicle API from 2s — 11 operation(s) for vehicle.
- [2s Watchers API](https://apis.io/apis/2s-io/2s-io-watchers-api/) — The watchers API from 2s — 27 operation(s) for watchers.
- [2s Water API](https://apis.io/apis/2s-io/2s-io-water-api/) — The water API from 2s — 1 operation(s) for water.
- [2s Weather API](https://apis.io/apis/2s-io/2s-io-weather-api/) — The weather API from 2s — 8 operation(s) for weather.
- [2s Wikidata API](https://apis.io/apis/2s-io/2s-io-wikidata-api/) — The wikidata API from 2s — 1 operation(s) for wikidata.
- [2s Wikipedia API](https://apis.io/apis/2s-io/2s-io-wikipedia-api/) — The wikipedia API from 2s — 1 operation(s) for wikipedia.
- [2s Word API](https://apis.io/apis/2s-io/2s-io-word-api/) — The word API from 2s — 2 operation(s) for word.
- [2s Worldbank API](https://apis.io/apis/2s-io/2s-io-worldbank-api/) — The worldbank API from 2s — 1 operation(s) for worldbank.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [2S Io Watchers Webhooks](https://apis.io/asyncapis/2s-io/2s-io-watchers-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [2s-io-mcp.yml](https://apis.io/servers/2s-io/2s-io-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [2S Io Agentic Access](https://apis.io/agentic-access/2s-io/2s-io-agentic-access/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [2S Io Openapi Overlay](https://apis.io/overlays/2s-io/2s-io-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [2S Io Authentication](https://apis.io/security/2s-io/2s-io-authentication/)
- [2S Io Domain Security](https://apis.io/security/2s-io/2s-io-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [2S Io Plans Pricing](https://apis.io/plans/2s-io/2s-io-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [2S Io Rate Limits](https://apis.io/rate-limits/2s-io/2s-io-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://2s.io/)
- [Documentation](https://2s.io/learn/x402)
- [Getting started](https://2s.io/learn/x402/quickstart)
- [API reference](https://2s.io/discover)
- [Pricing](https://2s.io/discover)
- [Support](https://github.com/2s-io/sdk/issues)
- [Changelog](https://2s.io/changelog.json)
- [GitHub](https://github.com/2s-io)
- [Status](https://2s.io/status)

## API Evangelist rating

**Kin Score 54.5** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 58.8 |
| Contract governance | 18.2 |
| Operational transparency | 76.3 |
| Developer ergonomics | 66.7 |
| Access clarity | 10.5 |

**Agent readiness 48.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | yes |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | conformant |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 16.7** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/2s-io/](https://apis.io/providers/2s-io/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for 2s: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/2s-io/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
