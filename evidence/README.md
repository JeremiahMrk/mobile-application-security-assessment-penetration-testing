# Evidence Handling

Only selected, sanitized evidence should be included in this public portfolio.

The original academic assessment contained technical screenshots and testing artifacts. Public evidence is intentionally limited to avoid exposing:

- authentication credentials,
- access or refresh tokens,
- cookies,
- authorization headers,
- personal information,
- user identifiers,
- private object/report identifiers,
- sensitive request or response bodies,
- exact exploitation sequences,
- reusable authentication material.

## Recommended Public Evidence

Safe examples include:

1. Sanitized JADX / manifest-review screenshot
2. Sanitized Burp Suite interface showing the testing workflow without sensitive request data
3. Sanitized ADB / local-storage evidence demonstrating encrypted-storage indicators
4. Sanitized JWT-validation evidence showing rejected tampered tokens

Screenshots should support the methodology without publishing unnecessary exploitation details.

## Redaction Standard

Before publishing any screenshot:

- Remove or blur tokens and cookies
- Remove passwords and account information
- Remove email addresses and personal identifiers
- Remove unique report or object identifiers
- Remove private hostnames if applicable
- Remove authorization headers
- Remove sensitive request/response bodies
- Verify the exported image again before publishing

When in doubt, omit the screenshot.
