# Vimeo OTT (vimeo-ott)

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
