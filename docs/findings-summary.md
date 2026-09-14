# Sanitized Findings Summary

The table below summarizes CVSS-scored findings from the final revised assessment.

Detailed exploitation instructions, raw requests, authentication material, private identifiers, and sensitive technical evidence are intentionally excluded from this public portfolio.

| ID | Finding | Source | CVSS v3.1 | Severity | Status |
|---|---|---|---:|---|---|
| D01 | Sensitive authentication data exposed through runtime logging | Dynamic | 8.4 | High | Confirmed |
| D02 | Private report comments accessible without valid authentication | Dynamic | 7.5 | High | Confirmed |
| D03 | Session/access token remains valid after logout | Dynamic | 8.1 | High | Confirmed |
| F01 | Insecure network configuration permitting cleartext traffic | Static | 5.4 | Medium | Static confirmed; runtime impact not confirmed |
| F02 | OAuth custom URI scheme with no static evidence of PKCE | Static | 6.8 | Medium | Potential; runtime behavior assessed separately |
| F03 | Potential OAuth authorization-code logging | Static | 6.1 | Medium | Potential |
| D04 | OAuth authorization request without PKCE parameter | Dynamic | 6.8 | Medium | Confirmed on tested request |
| D05 | Long-lived JWT and readable claims | Dynamic | 5.3 | Medium | Supporting evidence |
| F05 | Firebase / Google API configuration exposure | Static | 3.7 | Low | Potential |

## Main Risk Themes

### Authentication Data Exposure

Runtime logging exposed sensitive authentication-related data during testing, creating a potential credential and token exposure risk.

### Session Management

Testing showed that an existing authenticated token could remain usable after logout, indicating insufficient session revocation behavior in the tested environment.

### Access Control

A private-data access scenario was validated without valid authentication during the controlled assessment.

### OAuth Security

Static and dynamic observations identified weaknesses related to PKCE usage and sensitive OAuth-related logging.

### Configuration Security

Static analysis identified network and API configuration issues that warranted additional hardening.

## Interpretation

The results represent the behavior of the specific dummy/testing environment and application version assessed during the project.

They should not be interpreted as evidence that the same conditions currently exist in any production environment.
