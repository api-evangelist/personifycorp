# Personify (personifycorp)

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
