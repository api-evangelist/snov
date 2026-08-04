# Snov.io (snov)

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
