# Paragon Bank (paragon-bank)

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
