# DevSecOps Security Project – OWASP Juice Shop

## Overview
A hands-on cybersecurity project focused on web application vulnerability assessment, secure coding remediation, and automated security testing using OWASP Juice Shop.

## Objectives
- Identify and remediate web application vulnerabilities.
- Verify security fixes through retesting.
- Perform Static Application Security Testing (SAST).
- Explore automated security scanning in a CI/CD pipeline.

## My Contributions
- Tested four vulnerabilities: SQL Injection, IDOR (Broken Access Control), DOM-Based Cross-Site Scripting (XSS), and Improper Rating Validation.
- Investigated vulnerable code and applied security fixes.
- Retested vulnerabilities to verify the effectiveness of remediation.
- Used Semgrep to identify insecure coding patterns and compare scan results before and after remediation.

## Security Testing Results

| Activity | Result |
|---|---|
| SQL Injection | Remediated using a parameterized query |
| IDOR | Added server-side authorization checks |
| DOM-Based XSS | Improved safe handling of user input |
| Improper Rating Validation | Added server-side validation |
| Semgrep SAST | Findings decreased from 44 to 43 after remediation |

## Technologies Used
- OWASP Juice Shop
- Node.js
- Docker and Docker Compose
- Git and GitHub
- GitHub Actions
- Semgrep
- npm audit
- Gitleaks
- Trivy

## DevSecOps Pipeline
The project explored automated security checks in a GitHub Actions workflow:
- **Semgrep:** Static Application Security Testing (SAST)
- **npm audit:** Dependency vulnerability scanning
- **Gitleaks:** Potential secret detection
- **Trivy:** Container vulnerability scanning

Some security checks reported findings, demonstrating the importance of reviewing and addressing security risks.

## Key Learning Outcomes
- Web application vulnerability assessment
- Secure coding and vulnerability remediation
- Authorization and input validation
- Static code analysis
- CI/CD security integration
- Security testing and verification

## Disclaimer
This project was conducted for educational purposes using OWASP Juice Shop, an intentionally vulnerable web application. Testing was performed in a controlled environment.

## Acknowledgements
This was a collaborative university project based on OWASP Juice Shop. The contributions described above reflect my work on vulnerability assessment, remediation, and SAST analysis.
