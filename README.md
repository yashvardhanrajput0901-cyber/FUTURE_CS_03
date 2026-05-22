# API Security Risk Analysis

## Future Interns – Cyber Security Internship (Task 03)

This project presents a professional API Security Risk Analysis performed on public/demo REST APIs using ethical and read-only testing techniques.

The assessment focuses on identifying common API security weaknesses using the OWASP API Security Top 10 framework.

---

# Objective

The objective of this project is to:

- Analyze public APIs safely
- Inspect endpoints and responses
- Identify API security risks
- Assess authentication and authorization controls
- Evaluate security headers
- Classify risks based on severity
- Suggest remediation strategies

---

# APIs Tested

## 1. JSONPlaceholder API
https://jsonplaceholder.typicode.com

## 2. ReqRes API
https://reqres.in

---

# Tools Used

| Tool | Purpose |
|------|----------|
| Postman | API request testing |
| Browser DevTools | Header inspection |
| curl | Manual request testing |
| GitHub | Project hosting |
| PDF Report | Professional documentation |

---

# Testing Methodology

The following methodology was used during assessment:

1. Documentation Review
2. Endpoint Enumeration
3. Authentication Inspection
4. Response Analysis
5. Security Header Inspection
6. OWASP API Risk Mapping
7. Remediation Planning

---

# Security Risks Identified

| ID | Risk | Severity |
|----|------|----------|
| JP-001 | Missing Authentication | HIGH |
| JP-002 | Excessive Data Exposure | HIGH |
| JP-003 | Missing Rate Limiting | MEDIUM |
| JP-004 | IDOR Risk | HIGH |
| JP-005 | Missing Security Headers | MEDIUM |
| RR-001 | Weak Authentication Tokens | HIGH |
| RR-002 | Write Operations Without Auth | HIGH |
| RR-003 | Email Exposure | MEDIUM |
| RR-004 | Delay Parameter Abuse | MEDIUM |
| RR-005 | Missing HSTS/CORS Issues | MEDIUM |
| RR-006 | Mass Registration Risk | LOW |
| RR-007 | Sequential ID Enumeration | HIGH |

---

# OWASP API Security Top 10 Mapping

| OWASP Category | Finding |
|----------------|----------|
| API1 | IDOR / Sequential IDs |
| API2 | Broken Authentication |
| API3 | Excessive Data Exposure |
| API4 | No Rate Limiting |
| API5 | Broken Function Level Authorization |
| API6 | Mass Registration Abuse |
| API8 | Security Misconfiguration |

---

# Key Findings

## Missing Authentication
Several endpoints allowed unrestricted access without any authentication mechanism.

## Excessive Data Exposure
Sensitive user data including email addresses, phone numbers, addresses, and geolocation information were exposed publicly.

## IDOR Vulnerabilities
Sequential IDs enabled enumeration of user records and unauthorized data access patterns.

## Missing Security Headers
Important headers such as:
- Strict-Transport-Security
- X-Content-Type-Options
- Content-Security-Policy

were absent.

## Missing Rate Limiting
No API throttling or request limitation was observed.

---

# Business Impact

These vulnerabilities could lead to:

- Unauthorized data access
- Account takeover
- API abuse
- Data harvesting
- Phishing attacks
- Denial of Service (DoS)
- Regulatory compliance violations

---

# Remediation Recommendations

- Implement JWT/OAuth2 authentication
- Add role-based authorization
- Replace sequential IDs with UUIDs
- Apply field-level response filtering
- Implement API rate limiting
- Configure secure HTTP headers
- Add token expiry and refresh rotation
- Restrict CORS origins

---

# Repository Contents

```bash
report/         → Final PDF security report
screenshots/    → API testing screenshots
findings/       → Security findings documentation
assets/         → Project assets/images
```

---

# Ethical Scope

This project strictly followed ethical testing practices:

- Read-only testing only
- Public/demo APIs only
- No exploitation performed
- No bypass attempts
- No denial-of-service testing

---

# Author

Yashvardhan Rajput

Future Interns – Cyber Security Internship 2026

---

# Disclaimer

This project is intended solely for educational and internship demonstration purposes. All APIs tested are public/demo APIs designed for safe learning and experimentation.
