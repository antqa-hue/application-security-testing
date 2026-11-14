# Learning Roadmap

## Goal

Develop practical application security testing capability, progressing from security fundamentals to manual web and API testing, automated security checks, CI/CD integration and AI-assisted analysis.

The learning style is incremental: understand a concept, practise it in a safe lab, explain the result, and only then move forward.

## Stage 1 — Security fundamentals

**Objectives**
- Explain confidentiality, integrity and availability (CIA).
- Distinguish assets, threats, vulnerabilities, likelihood, impact and risk.
- Distinguish authentication from authorisation.
- Understand HTTP requests/responses, HTTPS, cookies and sessions at a conceptual level.
- Explain the purpose and limitations of the OWASP Top 10.

**Exit criteria**
- Complete the Stage 1 exercises.
- Correctly explain authentication vs authorisation.
- Identify assets, threats, vulnerabilities and likely impacts in a simple scenario.
- Explain why HTTPS does not by itself fix broken access control or weak authentication.

## Stage 2 — Manual web security testing

Study the OWASP Top 10 and relevant OWASP Web Security Testing Guide sections. Practise in PortSwigger Web Security Academy and local OWASP Juice Shop.

Topics include access control, authentication, injection, security misconfiguration, cryptographic failures, session handling and input/output handling.

**Exit criteria:** complete a set of beginner labs, document reproducible evidence, explain impact, and recommend remediation.

## Stage 3 — API security testing

Use OWASP API Security Top 10 and OWASP crAPI. Learn object-level and function-level authorisation, authentication, property-level authorisation, resource consumption, SSRF, inventory management and unsafe API consumption.

Introduce REST Assured and TestNG for repeatable positive and negative security tests. Keep security assertions separate from ordinary functional assertions where that improves clarity.

**Exit criteria:** produce a documented API security test suite against a local lab, including unauthorised and cross-user access scenarios.

## Stage 4 — Security automation

Introduce tools one at a time:
- DAST: OWASP ZAP.
- SAST: Semgrep Community Edition.
- SCA: OWASP Dependency-Check or another suitable free tool.
- Secrets detection: Gitleaks.
- Container/image scanning: Trivy, when containers are introduced.

Understand false positives, false negatives, severity, confidence, evidence and manual validation.

**Exit criteria:** run each selected tool locally, explain its output, triage findings and save safe reports.

## Stage 5 — DevSecOps

Integrate selected checks into GitHub Actions. Begin with non-blocking visibility, then introduce carefully defined quality gates. Preserve test reports and security artefacts without exposing secrets.

**Exit criteria:** a pull request workflow runs functional and security checks, reports findings, and fails only for agreed conditions.

## Stage 6 — AI-assisted security testing

Use AI to help derive test ideas from requirements and API specifications, explain findings, suggest remediation and draft reports. Validate all output manually. Do not let AI-generated tests or scanner output be treated as proof of security.

**Exit criteria:** demonstrate a repeatable human-reviewed AI-assisted workflow with traceable inputs, evidence and decisions.

## Suggested cadence

A flexible target is 1–3 focused learning sessions per week. Do not advance based only on elapsed time. Advance when the exit criteria are met.

## Core references

- [OWASP Top 10 2025](https://owasp.org/Top10/)
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
- [OWASP crAPI](https://owasp.org/www-project-crapi/)
