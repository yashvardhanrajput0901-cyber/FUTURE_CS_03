# API Security Risk Analysis

## Future Interns – Cyber Security Internship 2026

This repository contains a professional API Security Risk Analysis performed on public/demo APIs using ethical and read-only testing techniques.

The project focuses on identifying API security risks, evaluating implemented protections, and documenting findings using industry-standard security assessment methodology.

---

# Objective

The objective of this project was to:

- Analyze public/demo REST APIs
- Perform safe API security testing
- Inspect authentication mechanisms
- Review API responses and headers
- Identify security risks and exposures
- Evaluate implemented security protections
- Map findings with OWASP API Security Top 10
- Create a professional security assessment report

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
| curl | API request testing |
| jq | JSON formatting |
| Firefox DevTools | Header inspection |
| Kali Linux | Security testing environment |
| GitHub | Project hosting |
| Markdown | Documentation |
| PDF Report | Professional reporting |

---

# Testing Methodology

The following methodology was used:

1. API Documentation Review
2. Endpoint Enumeration
3. Authentication Inspection
4. Response Analysis
5. Header Inspection
6. Security Control Evaluation
7. OWASP API Top 10 Mapping
8. Remediation Planning

---

# Security Findings

| ID | Finding | Severity |
|----|----------|-----------|
| JP-001 | Missing Authentication | HIGH |
| JP-002 | Excessive Data Exposure | HIGH |
| JP-003 | Sequential ID Enumeration | MEDIUM |
| JP-004 | Public Exposure of PII | HIGH |
| JP-005 | Rate Limiting Present | INFO |
| JP-006 | Security Header Present | INFO |
| RR-001 | API Key Authentication Enforcement | INFO |
| RR-002 | Proper HTTP 401 Handling | INFO |
| RR-003 | Strong Security Header Configuration | INFO |

---

# Key Observations

## Missing Authentication

The JSONPlaceholder API allowed unrestricted access to user-related endpoints without authentication.

Example:
```bash
curl https://jsonplaceholder.typicode.com/users
```

---

## Excessive Data Exposure

Sensitive user-related information was publicly exposed, including:

- Email addresses
- Phone numbers
- Geolocation coordinates
- Company information
- Physical addresses

---

## Sequential ID Enumeration

Predictable object identifiers were observed:

```text
/users/1
/users/2
/users/3
```

This pattern may increase the risk of insecure direct object reference (IDOR) style vulnerabilities in real-world APIs.

---

## Rate Limiting Detected

The API included rate-limiting headers:

```text
x-ratelimit-limit
x-ratelimit-remaining
```

This helps mitigate API abuse and denial-of-service attacks.

---

## Security Headers Present

The APIs implemented several positive security controls, including:

- Strict-Transport-Security
- X-Content-Type-Options
- X-Frame-Options

---

## API Key Enforcement

ReqRes enforced authentication using API keys and correctly rejected unauthenticated requests using:

```text
HTTP/2 401 Unauthorized
```

---

# OWASP API Security Top 10 Mapping

| OWASP Category | Findings |
|----------------|----------|
| API1 | Sequential ID Enumeration |
| API2 | Missing Authentication |
| API3 | Excessive Data Exposure |
| API4 | Rate Limiting Controls |
| API8 | Security Header Configuration |

---

# Repository Structure

```bash
report/         → Final PDF report
raw-analysis/   → Raw API testing outputs
scripts/        → Bash automation scripts
screenshots/    → Evidence screenshots
findings/       → Security findings documentation
assets/         → Project assets
```

---

# Raw Analysis Included

The repository includes:

```text
raw-analysis/api_security_results.txt
```

This file contains:
- curl outputs
- header analysis
- API responses
- authentication responses
- security observations

---

# Automation Script Included

The repository also contains:

```bash
scripts/api_security_analysis.sh
```

This script automates:
- API testing
- response collection
- header analysis
- result logging

---

# Ethical Scope

This assessment strictly followed ethical testing principles:

- Read-only testing only
- Public/demo APIs only
- No exploitation performed
- No bypass attempts
- No denial-of-service testing

---

# Screenshots Included

The repository contains professional screenshots captured from:

- Kali Linux terminal
- curl-based testing
- Firefox DevTools
- Header analysis
- Response analysis

---

# Author

Yashvardhan Patel

Future Interns – Cyber Security Internship 2026

---

# Disclaimer

This project is intended strictly for educational and internship demonstration purposes. All APIs tested are public/demo APIs designed for safe learning and experimentation.
