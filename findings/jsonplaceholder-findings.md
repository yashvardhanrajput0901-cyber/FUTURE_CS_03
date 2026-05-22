# JSONPlaceholder API Findings

## API Tested
https://jsonplaceholder.typicode.com

---

## JP-001 — Missing Authentication

Severity: HIGH

Observation:
All endpoints including POST, PUT, and DELETE requests were accessible without authentication.

Risk:
Unauthorized users could access or manipulate data.

Remediation:
Implement JWT or OAuth2 authentication for all sensitive endpoints.

---

## JP-002 — Excessive Data Exposure

Severity: HIGH

Observation:
User responses exposed:
- Email
- Address
- Phone number
- Geolocation

Risk:
PII leakage and social engineering risk.

Remediation:
Return only required fields.

---

## JP-003 — Missing Rate Limiting

Severity: MEDIUM

Observation:
The /photos endpoint returned 5000 records without throttling.

Risk:
Potential API abuse and DoS attacks.

Remediation:
Implement pagination and rate limiting.

---

## JP-004 — IDOR Risk

Severity: HIGH

Observation:
Sequential IDs enabled access to multiple user records.

Risk:
Unauthorized access to other users’ data.

Remediation:
Implement authorization checks and UUIDs.

---

## JP-005 — Missing Security Headers

Severity: MEDIUM

Observation:
Security headers such as HSTS and CSP were absent.

Risk:
Increased attack surface.

Remediation:
Configure secure HTTP response headers.
