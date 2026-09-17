# Mobile Application Security Assessment — Academic Project (JAKI-themed Dummy APK)

Authorized, non-destructive mobile application security assessment of a dummy JAKI / Jakarta Kini Android APK conducted as an academic group project.

## Overview

This project combined Static Application Security Testing (SAST) and Dynamic Application Security Testing (DAST) to evaluate selected security properties of the dummy Android application.

Documented assessment context:

- Application: Dummy JAKI / Jakarta Kini Android APK
- Version: 4.0.19
- versionCode: 203
- Testing context: authorized, non-destructive
- Environment: dummy/testing environment and account
- Classification: OWASP/MASVS-related mapping and CVSS v3.1

The final revised assessment documented 3 High, 5 Medium, and 1 Low CVSS-scored findings, plus 4 positive/informational security observations. The highest documented severity was CVSS v3.1 8.4 (High).

## My Role

**Role: Technical Testing Coordinator**

My contribution focused primarily on the technical security-testing portion of the academic group project, including static and dynamic application analysis, vulnerability validation, technical evidence collection, and security finding assessment.

The final report and documentation were produced as a group project; this repository does not claim sole authorship of all project documentation.

## Methodology

### Static Analysis

- APK decompilation and code inspection
- AndroidManifest.xml review
- Resource and configuration review
- Static keyword searches
- OAuth-flow review
- Network-security configuration review

Primary tools and artifacts:

- JADX / JADX-GUI
- AndroidManifest.xml
- strings.xml
- network_security_config.xml

### Dynamic Analysis

- HTTP(S) traffic inspection
- Controlled request replay
- Authentication and session validation
- OAuth request review
- Runtime log inspection
- Local application-storage inspection

Primary tools:

- Burp Suite Community
- LDPlayer Android Emulator
- ADB / logcat
- JWT debugger

Sensitive tokens, cookies, identifiers, account data, and other private values were removed from the public portfolio.

## Assessment Results

Key risk areas included:

- Sensitive authentication information exposed through runtime logging
- Authentication/session invalidation weaknesses
- Access to private data without valid authentication
- OAuth / PKCE-related weaknesses
- Insecure network configuration
- Client-side API/Firebase configuration exposure

See [Sanitized Findings Summary](docs/findings-summary.md) for the public finding overview.

## Positive Security Observations

The assessment also documented controls that behaved correctly during testing, including:

- Encrypted local-storage indicators
- Rejection of modified and unsigned JWTs
- No plaintext JAKI user credential discovered in tested local-storage directories
- HTTPS observed during tested runtime flows

See [Positive Security Controls](docs/positive-security-controls.md).

## Remediation

Highest-priority recommendations included:

1. Prevent sensitive authentication data from being written to production logs
2. Implement server-side session/token revocation
3. Enforce authentication and authorization for private resources
4. Implement PKCE S256 for native OAuth flows

See [Remediation Priorities](docs/remediation-priorities.md).

## Repository Structure

- `docs/` - sanitized assessment summaries
- `evidence/` - public evidence-handling policy
- `report/` - recruiter-friendly public portfolio report
- `DISCLAIMER.md` - scope, ethics, and disclosure limitations

## Public Portfolio Report

A recruiter-friendly public summary is available here:

[Download / view the portfolio report](report/JAKI_Mobile_Security_Assessment_Portfolio.pdf)

## Important Scope Note

This repository represents an academic assessment conducted in an authorized dummy/testing context.

It must not be interpreted as a statement about the current security posture of the production JAKI application or infrastructure.

Detailed reproduction steps, sensitive identifiers, authentication material, exact private request data, and other potentially harmful information have intentionally been omitted from the public portfolio.

## Skills Demonstrated

- Mobile Application Security Testing
- Static Application Security Testing (SAST)
- Dynamic Application Security Testing (DAST)
- Android Application Analysis
- HTTP Traffic Analysis
- Authentication and Session Testing
- Vulnerability Validation
- Security Evidence Collection
- OWASP / MASVS Mapping
- CVSS v3.1 Assessment
- Security Remediation Analysis
