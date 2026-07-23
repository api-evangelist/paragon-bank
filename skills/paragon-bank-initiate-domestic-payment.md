---
name: Initiate a domestic payment (PIS)
description: Initiate a domestic payment (PIS)
api: openapi/obie-payment-initiation-standard.yaml
operations: ['CreateDomesticPaymentConsents', 'GetDomesticPaymentConsentsConsentId', 'GetDomesticPaymentConsentsConsentIdFundsConfirmation', 'CreateDomesticPayments', 'GetDomesticPaymentsDomesticPaymentId']
generated: '2026-07-23'
method: generated
---

## Initiate a Domestic Payment (OBIE PIS)

Standard OBIE Read/Write v4.0.1 flow for a PISP to set up and execute a single domestic payment.

### Steps
1. **Create payment consent** - `POST /domestic-payment-consents` (`CreateDomesticPaymentConsents`) with `Initiation` (creditor account, amount). Include `x-idempotency-key` and detached `x-jws-signature`.
2. **PSU authorises** - authorization-code + SCA; obtain the PSU token.
3. **Check funds (optional)** - `GET /domestic-payment-consents/{ConsentId}/funds-confirmation` (`GetDomesticPaymentConsentsConsentIdFundsConfirmation`).
4. **Confirm consent** - `GET /domestic-payment-consents/{ConsentId}` (`GetDomesticPaymentConsentsConsentId`) -> `Authorised`.
5. **Execute payment** - `POST /domestic-payments` (`CreateDomesticPayments`) referencing the ConsentId.
6. **Track status** - `GET /domestic-payments/{DomesticPaymentId}` (`GetDomesticPaymentsDomesticPaymentId`).

### Rules
- Scope: `payments`. Idempotency: `x-idempotency-key`, 24h retention; reuse with a changed body -> 409 (see `conventions/`).
- All initiation requests are JWS-signed. Errors -> `OBErrorResponse1` (see `errors/`).
- Note: OBIE standard; no confirmed Paragon PIS endpoint.
