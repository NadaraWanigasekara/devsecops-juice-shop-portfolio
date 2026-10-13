# CI/CD Security Pipeline

## Overview

This project used GitHub Actions to automate security checks as part of a DevSecOps workflow.

The workflow integrates security tools to identify potential issues in source code, dependencies, exposed secrets, and container images.

## Security Tools

### 1. Semgrep — SAST

Semgrep analyzes source code for potential insecure coding patterns without executing the application.

### 2. npm audit — Dependency Scanning

npm audit checks project dependencies against known security advisories.

### 3. Gitleaks — Secret Detection

Gitleaks scans repository content for potential exposed secrets. Findings require review to determine whether they represent actual secrets.

### 4. Trivy — Container Security

Trivy scans container images for known vulnerabilities. The configured pipeline uses a HIGH/CRITICAL severity threshold to determine whether the scan fails.

## Pipeline Results

- Semgrep completed successfully.
- npm audit was configured as a non-blocking check.
- Gitleaks reported 69 potential findings in a repository-wide scan.
- Trivy reported HIGH/CRITICAL image vulnerabilities in a separate pipeline run.

The Gitleaks and Trivy failures were observed in separate runs; they should not be represented as failures from the same run.

## Key Learning Outcomes

- Integrating security checks into GitHub Actions.
- Understanding security gates in a CI/CD workflow.
- Identifying dependency, secret, source-code, and container risks.
- Interpreting scan results and documenting remediation priorities.

## Limitations and Future Improvements

- Review and validate potential Gitleaks findings.
- Remediate dependency and container vulnerabilities.
- Consider adding Dynamic Application Security Testing (DAST), such as OWASP ZAP.
- Improve automated security regression testing.
