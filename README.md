# REKKI

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

REKKI is a food wholesale ordering platform that connects restaurants and chefs (buyers) with their suppliers. Restaurants place orders through the REKKI app, and suppliers receive, confirm, and fulfil them. REKKI publishes a public Supplier API that lets suppliers programmatically manage their product catalog (items, inventory, price lists), receive and confirm orders, report integration status back to REKKI, and manage REKKI Connect customers and their order guides. Authentication uses a supplier bearer token plus an X-REKKI-Authorization-Type header. REKKI's current product suite also includes AI agents for wholesale distributors (OrderAI, InboxAI, MenuAI) and a Marketplace. REKKI was surfaced as a portfolio company of Creandum and Point Nine.

**Areas:** Company · Food · Wholesale · Ordering · Restaurant · Supply Chain · Catalog · Order · E-Commerce

## REKKI on APIs.io

Everything profiled for REKKI is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/rekki/](https://apis.io/providers/rekki/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [REKKI Catalog API](https://apis.io/apis/rekki/rekki-catalog-api/) — The catalog API from REKKI — 12 operation(s) for catalog.
- [REKKI Connect Customers API](https://apis.io/apis/rekki/rekki-connect-customers-api/) — The connect_customers API from REKKI — 2 operation(s) for connect_customers.
- [REKKI General API](https://apis.io/apis/rekki/rekki-general-api/) — The general API from REKKI — 2 operation(s) for general.
- [REKKI Order Guide API](https://apis.io/apis/rekki/rekki-order-guide-api/) — The order-guide API from REKKI — 1 operation(s) for order-guide.
- [REKKI Orders API](https://apis.io/apis/rekki/rekki-orders-api/) — The orders API from REKKI — 11 operation(s) for orders.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [rekki-supplier-api](https://apis.io/servers/rekki/rekki-supplier-api/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Rekki Agentic Access](https://apis.io/agentic-access/rekki/rekki-agentic-access/)

#### Collections (5)

Postman and Open Collection request collections.

- [Rekki.com Supplier catalog API](https://apis.io/collections/rekki/open-rekki-catalog-api/)
- [Rekki.com Supplier catalog connect_customers API](https://apis.io/collections/rekki/open-rekki-connect-customers-api/)
- [Rekki.com Supplier catalog general API](https://apis.io/collections/rekki/open-rekki-general-api/)
- [Rekki.com Supplier catalog order-guide API](https://apis.io/collections/rekki/open-rekki-order-guide-api/)
- [Rekki.com Supplier catalog orders API](https://apis.io/collections/rekki/open-rekki-orders-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Rekki Supplier Api Overlay](https://apis.io/overlays/rekki/rekki-supplier-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Rekki Authentication](https://apis.io/security/rekki/rekki-authentication/)
- [Rekki Domain Security](https://apis.io/security/rekki/rekki-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://rekki.com/)
- [Documentation](https://github.com/rekki/supplier-api)
- [Getting started](https://rekki.com/suppliers)
- [API reference](https://api.rekki.com/swagger/index.html)
- [Support](https://rekki.com/faq)
- [Terms of service](https://rekki.com/terms-and-conditions)
- [Privacy policy](https://tandc.rekki.com/)
- [GitHub](https://github.com/rekki)

## API Evangelist rating

**Kin Score 38.9** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 44.0 |
| Contract governance | 4.5 |
| Operational transparency | 2.6 |
| Developer ergonomics | 54.2 |
| Access clarity | 21.1 |

**Agent readiness 23.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
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

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/rekki/](https://apis.io/providers/rekki/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for REKKI: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/rekki/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
