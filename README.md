# BitOasis

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

BitOasis is a Middle East and North Africa (MENA) cryptocurrency exchange, licensed as a Virtual Asset Service Provider by Dubai's Virtual Assets Regulatory Authority (VARA). It lets customers buy, sell, and trade Bitcoin, Ether, XRP, and other digital assets against the UAE Dirham (AED) and other fiat currencies. BitOasis exposes a public v1 Exchange REST API (https://api.bitoasis.net/v1) covering market data (markets, tickers, order books, trades) and authenticated account operations (balances, banks, Pro order placement and cancellation, and crypto and fiat deposits and withdrawals), authenticated with a Bearer API token. BitOasis also publishes an official open-source MCP server (bitoasis-mcp) that exposes the exchange as 23 tools for AI agents, over stdio or a hosted SSE endpoint. Originally added to the API Evangelist network as a pantera-capital portfolio lead, this profile has been enriched from BitOasis' first-party public developer surface.

**Areas:** Company · Cryptocurrency · Exchange · Trading · Digital Assets · Bitcoin · MENA · Fintech · MCP

## BitOasis on APIs.io

Everything profiled for BitOasis is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bitoasis/](https://apis.io/providers/bitoasis/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [BitOasis Account API](https://apis.io/apis/bitoasis/bitoasis-account-api/) — Authenticated account balances and registered banks.
- [BitOasis Coin Deposits API](https://apis.io/apis/bitoasis/bitoasis-coin-deposits-api/) — Digital-asset deposit history and address generation.
- [BitOasis Coin Withdrawals API](https://apis.io/apis/bitoasis/bitoasis-coin-withdrawals-api/) — Digital-asset withdrawal history, fees, and creation.
- [BitOasis Fiat Deposits API](https://apis.io/apis/bitoasis/bitoasis-fiat-deposits-api/) — Fiat deposit history.
- [BitOasis Fiat Withdrawals API](https://apis.io/apis/bitoasis/bitoasis-fiat-withdrawals-api/) — Fiat withdrawal history, creation, and cancellation.
- [BitOasis Market Data API](https://apis.io/apis/bitoasis/bitoasis-market-data-api/) — Public market data endpoints (no authentication required).
- [BitOasis Orders API](https://apis.io/apis/bitoasis/bitoasis-orders-api/) — Place, cancel, and read Pro exchange orders.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [bitoasis](https://apis.io/servers/bitoasis/bitoasis/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Bitoasis Agentic Access](https://apis.io/agentic-access/bitoasis/bitoasis-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [BitOasis Exchange Account API](https://apis.io/collections/bitoasis/open-bitoasis-account-api/)
- [BitOasis Exchange Account Coin Deposits API](https://apis.io/collections/bitoasis/open-bitoasis-coin-deposits-api/)
- [BitOasis Exchange Account Coin Withdrawals API](https://apis.io/collections/bitoasis/open-bitoasis-coin-withdrawals-api/)
- [BitOasis Exchange Account Fiat Deposits API](https://apis.io/collections/bitoasis/open-bitoasis-fiat-deposits-api/)
- [BitOasis Exchange Account Fiat Withdrawals API](https://apis.io/collections/bitoasis/open-bitoasis-fiat-withdrawals-api/)
- [BitOasis Exchange Account Market Data API](https://apis.io/collections/bitoasis/open-bitoasis-market-data-api/)
- [BitOasis Exchange Account Orders API](https://apis.io/collections/bitoasis/open-bitoasis-orders-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Bitoasis Exchange Overlay](https://apis.io/overlays/bitoasis/bitoasis-exchange-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Bitoasis Authentication](https://apis.io/security/bitoasis/bitoasis-authentication/)
- [Bitoasis Domain Security](https://apis.io/security/bitoasis/bitoasis-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://bitoasis.net/en/home)
- [Documentation](https://api.bitoasis.net/doc/)
- [Getting started](https://support.bitoasis.net/en/support/solutions/articles/29000035643-api-documentation)
- [API reference](https://api.bitoasis.net/doc/)
- [Support](https://support.bitoasis.net/)
- [Blog](https://bitoasis.net/blog/)
- [Compliance](https://bitoasis.net/en/page/legal-and-compliance)
- [Terms of service](https://bitoasis.net/en/page/terms-of-service)
- [Privacy policy](https://bitoasis.net/en/page/privacy-policy)
- [GitHub](https://github.com/bit-oasis)

## API Evangelist rating

**Kin Score 24.9** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 14.2 |
| Contract governance | 4.5 |
| Operational transparency | 2.6 |
| Developer ergonomics | 73.2 |
| Access clarity | 0.0 |

**Agent readiness 23.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bitoasis/](https://apis.io/providers/bitoasis/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for BitOasis: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bitoasis/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
