# Paragon Bank (paragon-bank)

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

Paragon Bank PLC is a UK specialist lender and retail savings bank, the principal banking subsidiary of Paragon Banking Group PLC (LSE: PAG), a FTSE 250 company founded in 1985 and headquartered in Solihull, West Midlands. Authorised by the Prudential Regulation Authority and regulated by the FCA and PRA (Firm Reference Number 604551, company number 05390593), Paragon offers fixed-rate and easy-access savings accounts and cash ISAs alongside buy-to-let and residential mortgages, second-charge mortgages, development finance, motor finance, and asset and commercial lending.

As a savings-and-lending institution rather than a personal current account provider, Paragon is **not one of the CMA9** and publishes **no public developer portal or Open Banking API surface of its own**. Its accounts are reachable to third parties only through account-information aggregators (e.g. Plaid, Tink, TrueLayer). This repository therefore represents the UK Open Banking Implementation Entity (OBIE) standard that an FCA-authorised ASPSP conforms to, captured verbatim from the OBIE specifications and **clearly labelled as unverified for this bank** — no Paragon-hosted endpoint was confirmed at profiling time.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/paragon-bank/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/paragon-bank/refs/heads/main/apis.yml)

## Tags

- Financial Services
- Banking
- Savings
- Mortgages
- Specialist Lender
- Open Banking
- PSD2
- OBIE
- United Kingdom
- Account Information

## Timestamps

- **Created:** 2026-07-23
- **Modified:** 2026-07-23

## APIs

> All API entries below are the **shared OBIE standard specifications**, not confirmed Paragon-hosted contracts. Paragon Bank does not document a developer portal, an Open Data endpoint, or Read/Write onboarding.

### Paragon Bank Open Data API (OBIE standard, unverified)

The UK Open Banking Open Data API — a public, unauthenticated reference-data surface (ATMs, branches, personal and business current accounts, unsecured SME loans, commercial credit cards) defined by the OBIE. Captured as the shared standard; Paragon publishes no confirmed Open Data endpoint and, without current accounts, has no CMA9 Open Data obligation.

- **Human URL:** [https://openbankinguk.github.io/opendata-api-docs-pub/v2.4.0/](https://openbankinguk.github.io/opendata-api-docs-pub/v2.4.0/)

#### Tags

- Open Data
- Reference Data
- Public

#### Properties

- [OpenAPI](openapi/obie-opendata-standard.json) — shared OBIE Open Data standard (Swagger 2.0)
- [Documentation](https://openbankinguk.github.io/opendata-api-docs-pub/v2.4.0/)
- [API Reference](https://github.com/OpenBankingUK/opendata-api-spec-compiled)

### Paragon Bank Account and Transaction Information API (OBIE standard, unverified)

The OBIE Read/Write Account and Transaction Information (AIS) API standard — FAPI-secured (OAuth2/OIDC, mutual-TLS, PSD2 strong customer authentication) account, balance, transaction, and party data access for authorised third parties. Shared OBIE standard, not a Paragon-hosted contract.

- **Human URL:** [Account and Transaction API Profile](https://openbankinguk.github.io/read-write-api-site3/v3.1.11/profiles/account-and-transaction-api-profile.html)

#### Tags

- Account Information
- Transactions
- AIS
- FAPI

#### Properties

- [OpenAPI](openapi/obie-account-info-standard.yaml) — shared OBIE Read/Write standard (OpenAPI 3.0)
- [Documentation](https://openbankinguk.github.io/read-write-api-site3/v3.1.11/profiles/account-and-transaction-api-profile.html)
- [API Reference](https://github.com/OpenBankingUK/read-write-api-specs)

### Paragon Bank Payment Initiation API (OBIE standard, unverified)

The OBIE Read/Write Payment Initiation (PIS) API standard — FAPI-secured initiation of domestic, scheduled, standing-order, international, and file payments with PSD2 strong customer authentication. Shared OBIE standard, not a Paragon-hosted contract; Paragon does not document payment-initiation services.

- **Human URL:** [Payment Initiation API Profile](https://openbankinguk.github.io/read-write-api-site3/v3.1.11/profiles/payment-initiation-api-profile.html)

#### Tags

- Payment Initiation
- Payments
- PIS
- FAPI

#### Properties

- [OpenAPI](openapi/obie-payment-initiation-standard.yaml) — shared OBIE Read/Write standard (OpenAPI 3.0)
- [Documentation](https://openbankinguk.github.io/read-write-api-site3/v3.1.11/profiles/payment-initiation-api-profile.html)
- [API Reference](https://github.com/OpenBankingUK/read-write-api-specs)

### Paragon Bank Confirmation of Funds API (OBIE standard, unverified)

The OBIE Read/Write Confirmation of Funds (CBPII) API standard — FAPI-secured yes/no confirmation of available funds for a card-based payment instrument issuer. Shared OBIE standard, not a Paragon-hosted contract.

- **Human URL:** [Confirmation of Funds API Profile](https://openbankinguk.github.io/read-write-api-site3/v3.1.11/profiles/confirmation-of-funds-api-profile.html)

#### Tags

- Confirmation of Funds
- CBPII
- FAPI

#### Properties

- [OpenAPI](openapi/obie-confirmation-funds-standard.yaml) — shared OBIE Read/Write standard (OpenAPI 3.0)
- [Documentation](https://openbankinguk.github.io/read-write-api-site3/v3.1.11/profiles/confirmation-of-funds-api-profile.html)
- [API Reference](https://github.com/OpenBankingUK/read-write-api-specs)

## Common Properties

- [Website](https://www.paragonbank.co.uk/)
- [About](https://www.paragonbank.co.uk/who-we-are)
- [Paragon Banking Group (parent)](https://www.paragonbankinggroup.co.uk/)
- [LinkedIn](https://uk.linkedin.com/company/paragon-banking-group-plc)
- [Support](https://www.paragonbank.co.uk/contact-us)
- [Savings rates](https://www.paragonbank.co.uk/savings)
- [Terms of Service](https://www.paragonbank.co.uk/resources/paragonbank/documents/savings/general-terms-and-conditions)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
