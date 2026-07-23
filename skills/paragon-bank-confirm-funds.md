---
name: Confirm available funds (CBPII)
description: Confirm available funds (CBPII)
api: openapi/obie-confirmation-funds-standard.yaml
operations: ['CreateFundsConfirmationConsents', 'GetFundsConfirmationConsentsConsentId', 'CreateFundsConfirmations']
generated: '2026-07-23'
method: generated
---

## Confirm Available Funds (OBIE CBPII)

Standard OBIE Read/Write v4.0.1 flow for a card-based payment instrument issuer to check funds availability.

### Steps
1. **Create funds-confirmation consent** - `POST /funds-confirmation-consents` (`CreateFundsConfirmationConsents`) with the debtor account.
2. **PSU authorises** - authorization-code + SCA.
3. **Confirm consent** - `GET /funds-confirmation-consents/{ConsentId}` (`GetFundsConfirmationConsentsConsentId`) -> `Authorised`.
4. **Check funds** - `POST /funds-confirmations` (`CreateFundsConfirmations`) with an amount -> boolean `FundsAvailable`.

### Rules
- Scope: `fundsconfirmations`. Auth: OBIE FAPI OAuth2 (see `authentication/`).
- Errors -> `OBErrorResponse1` (see `errors/`).
- Note: OBIE standard; no confirmed Paragon CBPII endpoint.
