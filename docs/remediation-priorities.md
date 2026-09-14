# Remediation Priorities

The final assessment prioritized remediation based on security impact and estimated implementation effort.

| Priority | Recommendation | Related Findings | Effort | Impact |
|---:|---|---|---|---|
| 1 | Disable sensitive BODY-level HTTP logging in production and restrict verbose logging to debug builds | D01 / F03 | Low | High |
| 2 | Implement server-side session/token revocation during logout | D03 / D05 | Medium | High |
| 3 | Require authentication and authorization checks for private report resources | D02 | Medium | High |
| 4 | Implement PKCE S256 for native OAuth flows | F02 / D04 | Medium | Medium |
| 5 | Remove unnecessary cleartext-traffic permissions and validate runtime transport security | F01 / D08 | Low-Medium | Medium |
| 6 | Restrict exposed Google/Firebase API configuration and review Firebase security rules | F05 | Low-Medium | Medium |

## Remediation Philosophy

The recommendations prioritize weaknesses that could expose authentication material or enable unauthorized access before lower-impact configuration issues.

The assessment also distinguishes between:

- confirmed runtime vulnerabilities,
- static security weaknesses,
- supporting evidence,
- positive security controls,
- and future-testing areas.

This prevents potential weaknesses from being presented as confirmed vulnerabilities without sufficient evidence.
