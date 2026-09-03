# Template Status & Verification

**Classification:** Configurable n8n template asset — not a verified production deployment.

This repository proves a version-controlled workflow structure and documented intended use. It does not by itself prove a current configured run, production reliability, SLA, ROI, or client outcome.

## Verification gate
1. Parse/import the JSON into a clean current n8n instance.
2. Inspect connections, expressions, IF/Switch branches, and Code nodes.
3. Replace every placeholder credential, URL, ID, model, webhook, table, channel, or resource reference.
4. Confirm current third-party API/version requirements.
5. Run a representative success case and at least one malformed-input/provider-failure case.
6. Confirm expected side effects/state and record the test date/result.

## Security
Never commit API keys, tokens, passwords, OAuth secrets, private webhooks, customer PII, or production data. Use synthetic test data and fresh test credentials.

## Change record
- **2026-09-03:** Added repository verification/security/status control. No workflow-logic change or runtime pass is implied.
