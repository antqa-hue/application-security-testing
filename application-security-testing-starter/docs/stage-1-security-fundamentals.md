# Stage 1 — Security Fundamentals

## Learning outcomes

By the end of this stage, you should be able to:
1. Explain confidentiality, integrity and availability.
2. Identify an asset, threat, vulnerability and risk.
3. Explain authentication vs authorisation.
4. Describe a basic HTTP request and response.
5. Explain what HTTPS protects and what it does not protect.
6. Describe why security testing needs both technical evidence and risk context.

## Lesson 1 — The CIA triad

The CIA triad is a simple model for three important security objectives.

### Confidentiality

Information should only be available to people and systems that are authorised to see it.

Example: one customer must not be able to view another customer's profile or order history.

Testing question: can a user retrieve data that belongs to another user?

### Integrity

Information should not be changed without appropriate authorisation.

Example: a standard customer should not be able to alter another customer's delivery address or account role.

Testing question: can a user modify data or security-sensitive properties they should not control?

### Availability

Systems and information should be available when needed by authorised users.

Example: an application should remain usable and resilient under expected demand.

Testing question: can a weakness or excessive request pattern make a service unavailable? For this learning project, study this concept; do not perform load or denial-of-service testing.

### Important distinction

A single vulnerability can affect more than one CIA objective. For example, unauthorised access to an account may affect confidentiality and integrity.

## Lesson 2 — Assets, threats, vulnerabilities and risk

- **Asset:** something valuable that needs protection, such as customer data, credentials, an API or a service.
- **Threat:** a potential cause of harm, such as an attacker, malicious insider, malware or accidental misuse.
- **Vulnerability:** a weakness that could be exploited, such as missing authorisation checks.
- **Impact:** the consequence if the weakness is exploited.
- **Likelihood:** how plausible exploitation is in the relevant context.
- **Risk:** a judgement that combines likelihood and impact, taking context into account.

A useful thinking chain is:

`Asset -> Threat -> Vulnerability -> Exploitation scenario -> Impact -> Risk`

Do not treat a scanner severity label as a complete risk assessment. Business context, exposure, exploitability and affected data matter.

## Lesson 3 — Authentication vs authorisation

**Authentication** answers: "Who are you?" It verifies an identity, often using a password, passkey, multi-factor authentication or a token.

**Authorisation** answers: "What are you allowed to do?" It decides whether an authenticated identity may perform a particular action on a particular resource.

Example:
- Alice signs in successfully: authentication succeeded.
- Alice requests order 123: the application must separately check whether Alice is authorised to view order 123.

A user being logged in does not mean they are allowed to access every record or function.

## Lesson 4 — HTTP and HTTPS basics

A browser or API client sends an HTTP request to a server. The server returns an HTTP response.

A request commonly includes:
- Method, such as GET, POST, PUT, PATCH or DELETE.
- Path, such as `/api/orders/123`.
- Headers, which carry metadata such as content type and authentication information.
- Optional body, often JSON for API requests.

A response commonly includes:
- Status code, such as 200, 201, 400, 401, 403 or 404.
- Headers.
- Optional body.

HTTPS is HTTP protected by TLS. It provides encryption in transit and helps authenticate the server. It does not automatically ensure that:
- The logged-in user is authorised to access a record.
- The application validates input safely.
- Password storage is secure.
- Business logic is correct.
- The server itself is free from vulnerabilities.

## Exercises

### Exercise A — CIA classification

For each scenario, identify the primary CIA objective affected. More than one may apply.

1. A customer can view another customer's invoice.
2. A user changes the price of an order without permission.
3. A service becomes unavailable because of a software defect.
4. An attacker obtains a password database.

Write your reasoning, not just the CIA letter.

### Exercise B — Identify the security concepts

Scenario: An online shop lets a signed-in customer change the numeric order ID in a URL. The server returns another customer's order without checking ownership.

Identify:
- The asset.
- The threat.
- The vulnerability.
- The likely impact.
- Which CIA objectives are affected.
- Whether the problem is authentication or authorisation, and why.

Do not attempt this against a real shop. This is a conceptual scenario; later we will reproduce similar behaviour in a local training lab.

### Exercise C — HTTPS misconception

A site uses HTTPS correctly, but a signed-in user can access another user's account by changing an identifier in the URL.

Explain why HTTPS does not prevent this issue.

### Exercise D — Short reflection

In your own words, explain why a successful functional login test is not enough to establish that authentication and authorisation are secure.

## Completion checklist

- [ ] I can explain confidentiality, integrity and availability with examples.
- [ ] I can distinguish assets, threats and vulnerabilities.
- [ ] I can explain authentication vs authorisation.
- [ ] I can describe a basic HTTP request and response.
- [ ] I can explain what HTTPS does and does not protect.
- [ ] I have written answers to Exercises A–D.
- [ ] I have reviewed my answers and recorded anything unclear.

## Free references for this stage

- [OWASP Top 10 2025](https://owasp.org/Top10/)
- [OWASP Web Security Testing Guide — Introduction](https://wstg.owasp.org/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
