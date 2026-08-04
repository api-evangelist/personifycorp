# Personify (personifycorp)

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

Personify (Personify Inc., part of Momentive Software as of January 2026) is a constituent and association management software provider for associations, nonprofits, and member-based organizations. Founded in 1996 and headquartered in Austin, Texas, Personify offers a family of products: the enterprise **Personify360 / ThreeSixty** AMS, **MemberClicks (MC Professional)** for mid-sized professional and trade associations, **Wild Apricot** for small associations and clubs, and **A2Z Events** for event management.

Several products expose documented REST APIs secured with OAuth 2.0. Wild Apricot and MemberClicks publish public developer documentation; Personify360's proprietary **Novus APIs** are documented via a Swagger (OpenAPI) interface but provisioned per customer through an account manager. **API access generally requires being a paying customer of the respective product** — there is no unified public self-serve developer portal or free API tier for the parent brand.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/personifycorp/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/personifycorp/refs/heads/main/apis.yml)

## Access Model

- **Customer/partner-gated.** Wild Apricot and MemberClicks REST APIs are documented publicly but require product account credentials (OAuth 2.0) to call.
- **Personify360 Novus API** access — the Swagger definition and base URL — is granted per customer through a Personify account manager, not published on a public portal.
- **Pricing is contact-sales** across all products (see `plans/`); API access is bundled with a subscription rather than sold as a standalone metered API.

## Tags

- Association Management
- AMS
- Membership
- Nonprofit
- Events
- Constituent Management
- CRM

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### Personify Wild Apricot API

RESTful API for the Wild Apricot small-association product, secured with OAuth 2.0 against base `https://api.wildapricot.org` (versioned paths such as `/v2.2/accounts/{accountId}/...`). Split into an admin API and a member API, it exposes contacts, accounts, membership levels, member groups, events, event registrations, invoices, and payments as JSON (or XML). Access requires Wild Apricot account credentials.

- **Human URL:** [https://gethelp.wildapricot.com/en/articles/182-using-wildapricot-s-api](https://gethelp.wildapricot.com/en/articles/182-using-wildapricot-s-api)
- **Base URL:** `https://api.wildapricot.org`

#### Tags

- Membership
- Contacts
- Events
- Invoices

#### Properties

- [Documentation](https://gethelp.wildapricot.com/en/articles/182-using-wildapricot-s-api)
- [API Reference](https://gethelp.wildapricot.com/en/categories/145-wild-apricot-member-api)

### Personify MemberClicks (MC Professional) API

JSON REST API for the MemberClicks MC Professional AMS, secured with OAuth 2.0. Base URL is organization-scoped (`https://{orgId}.memberclicks.net`) with resource paths under `/api/v1`, including member profiles, member types, and member statuses. Documented publicly in the MemberClicks help center; calls require an organization's API client credentials.

- **Human URL:** [https://help.memberclicks.com/hc/en-us/sections/14749781143437-API](https://help.memberclicks.com/hc/en-us/sections/14749781143437-API)
- **Base URL:** `https://{orgId}.memberclicks.net/api/v1`

#### Tags

- Membership
- Profiles
- OAuth

#### Properties

- [Documentation](https://help.memberclicks.com/hc/en-us/sections/14749781143437-API)
- [API Reference](https://help.memberclicks.com/hc/en-us/articles/15442876413197-API-Resources)

### Personify360 Novus API

Proprietary Novus API integration layer for the enterprise Personify360 / ThreeSixty AMS, documented with a Swagger (OpenAPI) interface for reporting, large-scale operations, and custom applications over Personify data. Logical resource areas follow the Personify360 modules — constituents (individuals, companies, donors, prospects), orders and products, events and meetings, certifications, and committees/subgroups. The Swagger definition and base URL are provisioned per customer through a Personify account manager rather than published publicly, so the base URL and endpoints are **modeled, not officially documented**. Personify360 also ships an older Personify API Library.

- **Human URL:** [https://personifycorp.com/blog/supercharge-your-data-insights-with-novus-apis/](https://personifycorp.com/blog/supercharge-your-data-insights-with-novus-apis/)
- **Base URL:** `https://api.personifycorp.com` *(modeled)*

#### Tags

- Constituents
- Orders
- Events
- Certifications
- Committees

#### Properties

- [Documentation](https://personifycorp.com/blog/supercharge-your-data-insights-with-novus-apis/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/personify-corp)
- [Website](https://personifycorp.com)
- [Documentation](https://gethelp.wildapricot.com/en/articles/182-using-wildapricot-s-api)
- [Plans](plans/personifycorp-plans-pricing.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
