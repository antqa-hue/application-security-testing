# Testing Scope and Safety Rules

## Purpose

Security testing can affect availability, data integrity and confidentiality. Every exercise must have a clear, authorised target and scope.

## Allowed practice targets

- A deliberately vulnerable application running locally, such as OWASP Juice Shop or OWASP crAPI.
- A system that you own and have configured specifically for testing.
- A third-party system only when explicit permission and written scope have been granted.

## Not allowed

- Scanning or exploiting random public websites, IP addresses, APIs or networks.
- Testing employer, client or production systems without explicit authorisation.
- Accessing, modifying, deleting or disclosing data belonging to other people.
- Running denial-of-service, destructive, persistence or stealth techniques as part of this learning path.
- Uploading credentials, tokens, session cookies, personal data or sensitive screenshots to GitHub or AI services.

## Before each practical exercise

Record:
- Target application and environment.
- Confirmation that the target is local or explicitly authorised.
- In-scope hosts, ports and paths.
- Out-of-scope actions.
- Test account(s) and test data.
- Expected impact and safe stop condition.

## Evidence handling

- Use synthetic accounts and data.
- Redact credentials, cookies, tokens, email addresses and personal information.
- Do not commit raw traffic containing secrets.
- Keep reports limited to the training environment.
- Stop immediately if the test behaves unexpectedly or reaches a system outside the agreed scope.

## Default project scope

For the initial stages, the only targets are local intentionally vulnerable training applications. Do not run scanners against public deployments of these projects.
