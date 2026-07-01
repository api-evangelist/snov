# Snov.io (snov)

Snov.io is a sales engagement platform providing email finder, email verification, prospect and list management, multichannel drip campaigns, sender account and warm-up management, and a lightweight sales CRM. Its REST API uses an OAuth2 client_credentials access token and mixes form-encoded v1 endpoints with a v2 asynchronous start/result (task_hash) pattern for search and verification.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/snov/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/snov/refs/heads/main/apis.yml)

## Tags

- Sales Engagement
- Email Finder
- Email Verification
- Prospecting
- Drip Campaigns
- CRM
- Lead Generation

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## Authentication

The Snov.io API uses the OAuth2 `client_credentials` grant. POST your API User ID (`client_id`) and API Secret (`client_secret`) to `https://api.snov.io/v1/oauth/access_token` to receive a Bearer `access_token` valid for 3600 seconds, then send it in the `Authorization` header on every request. The API is rate limited to 60 requests per minute.

## APIs

### Snov.io Authentication API

Exchanges an API User ID (client_id) and API Secret (client_secret) for a Bearer access token via the OAuth2 client_credentials grant. Tokens are valid for one hour and must be sent on every subsequent request.

- **Human URL:** [https://snov.io/api](https://snov.io/api)
- **Base URL:** `https://api.snov.io/v1`

#### Tags

- OAuth2
- Access Token
- Authentication

#### Properties

- [Documentation](https://snov.io/api)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Email Finder API

Finds verified business emails from a prospect first name, last name, and company domain using the asynchronous emails-by-domain-by-name start/result (task_hash) pattern, plus company-domain-by-name lookup.

- **Human URL:** [https://snov.io/email-finder-api](https://snov.io/email-finder-api)
- **Base URL:** `https://api.snov.io/v2`

#### Tags

- Email Finder
- Domain Search
- Enrichment

#### Properties

- [Documentation](https://snov.io/knowledgebase/how-to-get-email-contacts-from-a-list-of-names/)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Domain Search API

Returns company information, prospect profiles, domain emails, and generic contacts (sales@, info@) for a given domain via asynchronous start/result tasks, plus a free domain email count endpoint.

- **Human URL:** [https://snov.io/knowledgebase/how-to-use-domain-search-api/](https://snov.io/knowledgebase/how-to-use-domain-search-api/)
- **Base URL:** `https://api.snov.io/v2`

#### Tags

- Domain Search
- Prospects
- Company Data

#### Properties

- [Documentation](https://snov.io/knowledgebase/how-to-use-domain-search-api/)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Email Verifier API

Verifies up to ten email addresses per request with multistep SMTP, format, disposable, webmail, and gibberish checks, returning valid, not_valid, or unknown status via the start/result (task_hash) pattern.

- **Human URL:** [https://snov.io/email-verifier](https://snov.io/email-verifier)
- **Base URL:** `https://api.snov.io/v2`

#### Tags

- Email Verification
- Deliverability
- SMTP

#### Properties

- [Documentation](https://snov.io/knowledgebase/how-to-use-snov-io-api/)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Enrichment API

Enriches contacts with full profile data from an email address (v1 get-profile-by-email) or from LinkedIn member URLs (v2 li-profiles-by-urls), returning name, position, company, social, and location data.

- **Human URL:** [https://snov.io/knowledgebase/how-to-enrich-your-data-via-snov-io-api/](https://snov.io/knowledgebase/how-to-enrich-your-data-via-snov-io-api/)
- **Base URL:** `https://api.snov.io/v2`

#### Tags

- Enrichment
- Profile Lookup
- LinkedIn

#### Properties

- [Documentation](https://snov.io/knowledgebase/how-to-enrich-your-data-via-snov-io-api/)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Prospects & Lists API

Creates and reads prospect lists, adds prospects to a list, and looks up prospects by id or email so contacts can be organized and pushed into drip campaigns.

- **Human URL:** [https://snov.io/api](https://snov.io/api)
- **Base URL:** `https://api.snov.io/v1`

#### Tags

- Prospects
- Lists
- CRM

#### Properties

- [Documentation](https://snov.io/api)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Drip Campaigns API

Lists a user's campaigns and pulls per-campaign engagement reporting - emails sent, opened, clicked, and replied - for multichannel drip outreach analytics.

- **Human URL:** [https://snov.io/email-drip-campaigns](https://snov.io/email-drip-campaigns)
- **Base URL:** `https://api.snov.io/v1`

#### Tags

- Drip Campaigns
- Outreach
- Analytics

#### Properties

- [Documentation](https://snov.io/knowledgebase/email-drip-campaigns/)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Sender Accounts API

Connects, updates, lists, and checks the SMTP/IMAP status of email sender accounts used to send campaigns, including daily limits, signatures, and sending delays.

- **Human URL:** [https://snov.io/api](https://snov.io/api)
- **Base URL:** `https://api.snov.io/v2`

#### Tags

- Sender Accounts
- SMTP
- Deliverability

#### Properties

- [Documentation](https://snov.io/api)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io Email Warm-up API

Creates, lists, reads, and updates email warm-up campaigns that gradually build sender reputation using progressive or steady strategies with configurable daily goals and reply rates.

- **Human URL:** [https://snov.io/api](https://snov.io/api)
- **Base URL:** `https://api.snov.io/v2`

#### Tags

- Warm-up
- Deliverability
- Reputation

#### Properties

- [Documentation](https://snov.io/api)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Snov.io User & Balance API

Reports the account's current credit balance and plan usage for free, letting integrations check remaining credits before running metered search and verification calls.

- **Human URL:** [https://snov.io/api](https://snov.io/api)
- **Base URL:** `https://api.snov.io/v1`

#### Tags

- User
- Balance
- Credits

#### Properties

- [Documentation](https://snov.io/api)
- [OpenAPI](openapi/snov-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/snov.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/snov.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/snov-io)
- [Website](https://snov.io)
- [Documentation](https://snov.io/api)
- [Plans](plans/snov-plans-pricing.yml)
- [Rate Limits](rate-limits/snov-rate-limits.yml)
- [Fin Ops](finops/snov-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
