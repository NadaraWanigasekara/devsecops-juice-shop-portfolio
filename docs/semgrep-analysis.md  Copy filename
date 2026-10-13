# Semgrep SAST Analysis

## Overview

Static Application Security Testing (SAST) analyzes source code to identify potential security issues without executing the application.

In this project, I used Semgrep with the OWASP Top Ten ruleset to analyze insecure coding patterns.

## Before and After Remediation

| Stage | Findings |
|---|---:|
| Initial scan | 44 |
| After remediation | 43 |

The finding count decreased after the SQL Injection remediation in `routes/login.ts`.

## Remediation

The vulnerable login query was updated to use a parameterized query. This separates SQL commands from user-supplied input and helps prevent SQL Injection.

## Targeted Scan

A targeted scan of the following security-sensitive files returned zero findings:

- `routes/login.ts`
- `routes/basket.ts`
- `models/feedback.ts`
- `frontend/src/app/search-result/search-result.component.ts`

## Results and Limitations

The reduction from 44 to 43 findings indicates that one related Sequelize injection finding was no longer reported after remediation.

Static analysis results require review because findings may need validation, and a scan with zero findings does not guarantee that an application is completely secure.

## Skills Demonstrated

- Static Application Security Testing (SAST)
- Semgrep
- Secure coding remediation
- Source-code security analysis
- Before-and-after verification
