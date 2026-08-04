# Vimeo OTT (vimeo-ott)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Vimeo OTT (formerly **VHX**) is a subscription video / over-the-top (OTT) platform for launching branded SVOD, TVOD, and live streaming services across web, mobile, and connected-TV apps. Its documented REST API at `https://api.vhx.tv` lets media companies programmatically manage customers, products (subscription, rental, and purchase access agreements), videos, and collections (categories, series, seasons, movies, playlists), plus watchlists, player authorizations, comments, live events, and analytics.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vimeo-ott/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vimeo-ott/refs/heads/main/apis.yml)

## Access Model

- The API is **publicly documented** at [dev.vhx.tv](https://dev.vhx.tv/docs/api/) — the reference is open to read without an account.
- **Authentication** is HTTP **Basic Auth**: your Vimeo OTT API key is supplied as the username and the password is left blank. API keys are created on the **Platforms** page of your Vimeo OTT CMS.
- Using the API in practice requires a **paid Vimeo OTT account** (Starter or Enterprise). The API is a management surface for an OTT service you operate on the platform — there is no free, standalone, self-serve API product. In that sense the useful API is **plan-gated behind an OTT subscription**, even though the docs are public.
- All access is over **HTTPS**; requests and responses are **JSON**, using the HAL hypermedia convention (`_links`, `_embedded`). Timestamps are ISO 8601 (UTC), encoding is UTF-8, and JSONP is supported via a `?callback=` parameter.
- List endpoints are **paginated** (default 50 items per page).

The endpoints documented here are **confirmed from the live public API reference** (methods and paths). The bundled OpenAPI and collection artifacts **model the request/response schemas** where the reference documents fields by example rather than as a formal schema; those bodies are flagged as modeled.

## Tags

- OTT
- Video
- SVOD
- Streaming
- Media
- Subscriptions
- VHX

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Vimeo OTT Customers API

Create, retrieve, list, and update customers (subscribers), grant and revoke per-product access, and manage each customer's watchlist and in-progress "watching" list. Customer-scoped requests are made with the `VHX-Customer` and `VHX-Client-IP` headers.

- **Human URL:** [https://dev.vhx.tv/docs/api/](https://dev.vhx.tv/docs/api/)
- **Base URL:** `https://api.vhx.tv`

#### Tags

- Customers
- Subscribers
- Watchlist

#### Properties

- [Documentation](https://dev.vhx.tv/docs/api/)
- [API Reference](https://dev.vhx.tv/docs/api/)
- [OpenAPI](openapi/vimeo-ott-openapi.yml)
- [Postman Collection](collections/vimeo-ott.postman_collection.json)
- [Open Collection](collections/vimeo-ott.opencollection.json)

### Vimeo OTT Products API

Retrieve and list products — the access agreements (subscription, rental, or purchase) that bundle videos and collections — and fetch a product's prices across multiple currencies.

- **Human URL:** [https://dev.vhx.tv/docs/api/](https://dev.vhx.tv/docs/api/)
- **Base URL:** `https://api.vhx.tv`

#### Tags

- Products
- Access
- Pricing

#### Properties

- [Documentation](https://dev.vhx.tv/docs/api/)
- [API Reference](https://dev.vhx.tv/docs/api/)
- [OpenAPI](openapi/vimeo-ott-openapi.yml)
- [Postman Collection](collections/vimeo-ott.postman_collection.json)
- [Open Collection](collections/vimeo-ott.opencollection.json)

### Vimeo OTT Videos API

Create, retrieve, list, update, and delete videos, and access the playable adaptive-streaming file URLs for a video. Videos are the transcoded content items surfaced through the OTT storefront and player.

- **Human URL:** [https://dev.vhx.tv/docs/api/](https://dev.vhx.tv/docs/api/)
- **Base URL:** `https://api.vhx.tv`

#### Tags

- Videos
- Files
- Content

#### Properties

- [Documentation](https://dev.vhx.tv/docs/api/)
- [API Reference](https://dev.vhx.tv/docs/api/)
- [OpenAPI](openapi/vimeo-ott-openapi.yml)
- [Postman Collection](collections/vimeo-ott.postman_collection.json)
- [Open Collection](collections/vimeo-ott.opencollection.json)

### Vimeo OTT Collections API

Create, retrieve, list, and update collections — categories, series, seasons, movies, and playlists — and manage their items, including adding, removing, and repositioning videos and nested collections, plus reordering the collection itself.

- **Human URL:** [https://dev.vhx.tv/docs/api/](https://dev.vhx.tv/docs/api/)
- **Base URL:** `https://api.vhx.tv`

#### Tags

- Collections
- Series
- Playlists

#### Properties

- [Documentation](https://dev.vhx.tv/docs/api/)
- [API Reference](https://dev.vhx.tv/docs/api/)
- [OpenAPI](openapi/vimeo-ott-openapi.yml)
- [Postman Collection](collections/vimeo-ott.postman_collection.json)
- [Open Collection](collections/vimeo-ott.opencollection.json)

### Vimeo OTT Authorizations API

Generate short-lived authorization tokens that grant a specific customer access to an embeddable video player, with configurable session token expiration.

- **Human URL:** [https://dev.vhx.tv/docs/api/](https://dev.vhx.tv/docs/api/)
- **Base URL:** `https://api.vhx.tv`

#### Tags

- Authorizations
- Player
- Embed

#### Properties

- [Documentation](https://dev.vhx.tv/docs/api/)
- [Player Documentation](https://dev.vhx.tv/player/)
- [OpenAPI](openapi/vimeo-ott-openapi.yml)
- [Postman Collection](collections/vimeo-ott.postman_collection.json)
- [Open Collection](collections/vimeo-ott.opencollection.json)

### Vimeo OTT Analytics API

Retrieve performance reports for an OTT service, including traffic, income, units sold, subscribers, churn, and per-video metrics.

- **Human URL:** [https://dev.vhx.tv/docs/api/](https://dev.vhx.tv/docs/api/)
- **Base URL:** `https://api.vhx.tv`

#### Tags

- Analytics
- Reporting
- Metrics

#### Properties

- [Documentation](https://dev.vhx.tv/docs/api/)
- [API Reference](https://dev.vhx.tv/docs/api/)
- [OpenAPI](openapi/vimeo-ott-openapi.yml)
- [Postman Collection](collections/vimeo-ott.postman_collection.json)
- [Open Collection](collections/vimeo-ott.opencollection.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/vimeo)
- [Website](https://vimeo.com/ott)
- [Documentation](https://dev.vhx.tv/docs/api/)
- [GitHub Organization](https://github.com/vhx)
- [Plans](plans/vimeo-ott-plans-pricing.yml)
- [Rate Limits](rate-limits/vimeo-ott-rate-limits.yml)
- [Fin Ops](finops/vimeo-ott-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
