---
name: Access customer account and transaction data (AIS)
description: Access customer account and transaction data (AIS)
api: openapi/obie-account-info-standard.yaml
operations: ['CreateAccountAccessConsents', 'GetAccountAccessConsentsConsentId', 'GetAccounts', 'GetAccountsAccountIdBalances', 'GetAccountsAccountIdTransactions']
generated: '2026-07-23'
method: generated
---

## Access Account & Transaction Information (OBIE AIS)

Standard OBIE Read/Write v4.0.1 flow for an AISP to read a PSU account data. Requires a FAPI-secured client (mutual-TLS, signed requests) and PSU strong customer authentication.

### Steps
1. **Create the consent** - `POST /account-access-consents` (`CreateAccountAccessConsents`) with the requested `Permissions` (e.g. `ReadAccountsDetail`, `ReadBalances`, `ReadTransactionsDetail`). Use a TPP client-credentials token. Send `x-fapi-interaction-id` for tracing.
2. **PSU authorises** - redirect the customer through the ASPSP authorization-code + SCA flow; exchange for a PSU access token.
3. **Confirm consent** - `GET /account-access-consents/{ConsentId}` (`GetAccountAccessConsentsConsentId`) -> status `Authorised`.
4. **List accounts** - `GET /accounts` (`GetAccounts`).
5. **Read balances / transactions** - `GET /accounts/{AccountId}/balances` (`GetAccountsAccountIdBalances`), `GET /accounts/{AccountId}/transactions` (`GetAccountsAccountIdTransactions`). Page via `Links.Next` / `Meta.TotalPages`.

### Rules
- Scope: `accounts`. Auth: OBIE FAPI OAuth2. See `authentication/` and `scopes/`.
- Errors use the `OBErrorResponse1` envelope (see `errors/`). 403 = consent/scope mismatch; 401 = re-authenticate.
- Note: this is the OBIE standard; Paragon Bank exposes no confirmed AIS endpoint.
