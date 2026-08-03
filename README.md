# Atomic (atomic-fi)

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

Atomic is a payroll and financial connectivity platform. Through user-permissioned access to payroll, HR, and merchant accounts, Atomic lets applications switch direct deposit, verify income and employment, retrieve payroll data, and update payment methods on file. The Transact SDK is an embedded, hosted front-end that drives these workflows on top of Atomic's backend REST API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/atomic-fi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/atomic-fi/refs/heads/main/apis.yml)

## Tags

- Fintech
- Payroll
- Direct Deposit
- Income Verification
- Employment Verification
- Financial Connectivity
- Embedded Finance

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### Atomic Access Tokens API

Exchanges your API Key and Secret for a short-lived publicToken that initializes the Transact SDK on the client. Includes creating and revoking access tokens, called from your backend so credentials never reach the browser.

- **Human URL:** [https://docs.atomicfi.com/reference/api](https://docs.atomicfi.com/reference/api)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Access Tokens
- Authentication
- Public Token

#### Properties

- [Documentation](https://docs.atomicfi.com/reference/api)
- [API Reference](https://docs.atomicfi.com/reference/api)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atomic-fi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atomic-fi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Atomic Transact SDK

Embedded, hosted front-end (Browser, iOS, Android, React Native, Flutter, Capacitor, WebView) launched with Atomic.transact() and a publicToken. It runs deposit, verify, and tax task workflows, handling user authentication and consent, and emits client-side events (onFinish, onClose, onInteraction, onTaskStatusUpdate) over Atomic's backend API.

- **Human URL:** [https://docs.atomicfi.com/reference/transact-sdk](https://docs.atomicfi.com/reference/transact-sdk)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Transact
- SDK
- Embedded
- Front End

#### Properties

- [Documentation](https://docs.atomicfi.com/reference/transact-sdk)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Atomic Tasks API

Retrieves task details and status, generates presigned file URLs, runs task prescreen confidence checks, and starts task workflows from an existing linked account. Tasks are the unit of work behind deposit, verify, and tax operations.

- **Human URL:** [https://docs.atomicfi.com/reference/api](https://docs.atomicfi.com/reference/api)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Tasks
- Task Workflow
- Status

#### Properties

- [Documentation](https://docs.atomicfi.com/reference/api)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atomic-fi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atomic-fi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Atomic Deposit API

Switches a user's direct deposit at their payroll or HR provider, supporting total, fixed, and percent distribution splits. Surfaced through the deposit task operation and exposes the user's current deposit accounts on file.

- **Human URL:** [https://docs.atomicfi.com/products/deposit/implementation](https://docs.atomicfi.com/products/deposit/implementation)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Deposit
- Direct Deposit Switch
- Distribution

#### Properties

- [Documentation](https://docs.atomicfi.com/products/deposit/implementation)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Atomic Verify API

Verifies income and employment via the verify task operation, returning employment status, income (annual/hourly, pay cycle, next pay date), identity, statements/paystubs, timesheets, and taxes (W-2 / 1099) pulled from the connected payroll system.

- **Human URL:** [https://docs.atomicfi.com/products/verify/implementation](https://docs.atomicfi.com/products/verify/implementation)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Verify
- Income
- Employment
- Identity

#### Properties

- [Documentation](https://docs.atomicfi.com/products/verify/implementation)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Atomic PayLink API

User-permissioned access into merchants and subscription services to read and update payment methods on file, and to run account actions such as pausing or canceling a plan. Card data flows through a dedicated PCI host (pci.atomicfi.com).

- **Human URL:** [https://docs.atomicfi.com/paylink/reference/api](https://docs.atomicfi.com/paylink/reference/api)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- PayLink
- Manage Payments
- Cards on File
- Subscriptions

#### Properties

- [Documentation](https://docs.atomicfi.com/paylink/reference/api)
- [API Reference](https://docs.atomicfi.com/paylink/reference/api)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Atomic Data & Transactions API

Retrieves payroll data by user identifier - deposit accounts, employment, identity, income, statements, timesheets, and taxes - plus linked-account listing and user/monitoring management for ongoing connections.

- **Human URL:** [https://docs.atomicfi.com/reference/api](https://docs.atomicfi.com/reference/api)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Data
- Payroll Data
- Statements
- Linked Accounts

#### Properties

- [Documentation](https://docs.atomicfi.com/reference/api)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/atomic-fi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/atomic-fi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Atomic Webhooks API

Manages webhook endpoints and signing secrets, and delivers real-time CloudEvents-formatted notifications such as task-status-updated, payroll-data-fetched, and the *-synced data events, with retries and manual replay.

- **Human URL:** [https://docs.atomicfi.com/reference/webhooks](https://docs.atomicfi.com/reference/webhooks)
- **Base URL:** `https://api.atomicfi.com`

#### Tags

- Webhooks
- Events
- CloudEvents

#### Properties

- [Documentation](https://docs.atomicfi.com/reference/webhooks)
- [OpenAPI](openapi/atomic-fi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/atomicfi)
- [LinkedIn](https://www.linkedin.com/company/atomicfi)
- [Website](https://atomicfi.com)
- [Documentation](https://docs.atomicfi.com)
- [Plans](plans/atomic-fi-plans-pricing.yml)
- [Rate Limits](rate-limits/atomic-fi-rate-limits.yml)
- [Fin Ops](finops/atomic-fi-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
