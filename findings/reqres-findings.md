# ReqRes API Findings

## RR-001 — API Key Authentication Enforcement

Severity: INFO

Observation:
API rejected unauthenticated requests.

Evidence:
HTTP 401 Unauthorized

Security Benefit:
Prevents anonymous access.

---

## RR-002 — Proper HTTP 401 Handling

Severity: INFO

Observation:
Authentication failures returned proper status codes.

Security Benefit:
Correct authentication handling.

---

## RR-003 — Strong Security Header Configuration

Severity: INFO

Observed Headers:
- Strict-Transport-Security
- X-Frame-Options
- X-Content-Type-Options

Security Benefit:
Improves API security posture.
