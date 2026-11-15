# Security guidelines

Apply controls according to the threat model and data sensitivity.

- Validate untrusted input at every system boundary.
- Enforce authorization server-side for each protected operation and object.
- Hash passwords using a vetted password-hashing algorithm/library; never store plaintext.
- Protect sessions/tokens with appropriate expiry, storage, rotation, and revocation.
- Restrict CORS in deployed environments.
- Use HTTPS in production.
- Store secrets in environment or secret-management systems; never commit them.
- Use least-privilege service/database accounts.
- Prevent injection with parameterized queries/ORM APIs.
- Consider XSS, CSRF, SSRF, IDOR, upload abuse, rate abuse, and account enumeration where relevant.
- Limit and validate uploads; use safe storage names and isolate uploaded content.
- Avoid logging credentials, tokens, sensitive personal data, or private model prompts.
- Keep dependencies updated and review known vulnerabilities.
- Return safe error messages without stack traces or internal configuration.
- Document security controls that are implemented and tested; never make blanket “secure” claims.
