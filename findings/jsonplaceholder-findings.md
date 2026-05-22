# JSONPlaceholder API Findings

## JP-001 — Missing Authentication

Severity: HIGH

Observation:
User endpoints were publicly accessible without authentication.

Risk:
Unauthorized users can access sensitive user-related data.

---

## JP-002 — Excessive Data Exposure

Severity: HIGH

Exposed Data:
- Email
- Phone Number
- Address
- Geolocation
- Company Details

Risk:
Potential privacy exposure and data harvesting.

---

## JP-003 — Sequential ID Enumeration

Severity: MEDIUM

Observation:
Sequential numeric identifiers were used.

Example:
- /users/1
- /users/2

Risk:
Potential IDOR-style access patterns.

---

## JP-004 — Public Exposure of PII

Severity: HIGH

Observation:
Personally identifiable information was publicly accessible.

Risk:
Social engineering and phishing exposure.

---

## JP-005 — Rate Limiting Present

Severity: INFO

Observation:
Rate limiting headers were detected.

Security Benefit:
Helps mitigate abuse and automated attacks.

---

## JP-006 — Security Headers Present

Severity: INFO

Observed Headers:
- X-Content-Type-Options

Security Benefit:
Improves browser security posture.
