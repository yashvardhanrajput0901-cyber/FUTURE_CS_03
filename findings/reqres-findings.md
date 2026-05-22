# ReqRes API Findings

## API Tested
https://reqres.in

---

## RR-001 — Weak Authentication Tokens

Severity: HIGH

Observation:
Authentication tokens lacked expiry and rotation.

Risk:
Permanent token compromise.

Remediation:
Use JWT with expiry and refresh tokens.

---

## RR-002 — Write Operations Without Authentication

Severity: HIGH

Observation:
PUT and DELETE requests succeeded without auth tokens.

Risk:
Unauthorized data modification.

Remediation:
Require bearer token validation.

---

## RR-003 — User Email Exposure

Severity: MEDIUM

Observation:
Public user email exposure observed.

Risk:
Phishing and user enumeration.

Remediation:
Restrict email visibility.

---

## RR-004 — Delay Parameter Abuse

Severity: MEDIUM

Observation:
Delay parameters could hold server connections open.

Risk:
Potential resource exhaustion.

Remediation:
Limit request duration and remove unnecessary delay functionality.

---

## RR-005 — Missing HSTS and CORS Issues

Severity: MEDIUM

Observation:
Wildcard CORS and missing HSTS headers observed.

Risk:
Cross-origin abuse and SSL stripping.

Remediation:
Whitelist trusted origins and enforce HTTPS.

---

## RR-006 — Mass Registration Risk

Severity: LOW

Observation:
Registration accepted arbitrary emails without verification.

Risk:
Spam account creation.

Remediation:
Implement email verification and CAPTCHA.

---

## RR-007 — Sequential User ID Enumeration

Severity: HIGH

Observation:
Predictable IDs enabled user enumeration.

Risk:
User database harvesting.

Remediation:
Use UUID-based identifiers.
