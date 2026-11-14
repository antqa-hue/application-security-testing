# Application Security Testing

A practical, step-by-step learning and portfolio project covering application security testing, API security, security automation, DevSecOps, and AI-assisted security analysis.

## Learning approach

This repository is both a learning journal and an evolving technical portfolio. Work through one stage at a time. Each stage should include:

1. Concepts explained in your own words.
2. A practical exercise in an authorised lab.
3. Evidence and observations.
4. A clear explanation of impact and remediation.
5. A review before moving to the next stage.

## Learning roadmap

| Stage | Focus | Main outcome |
|---|---|---|
| 1 | Security fundamentals | Explain core security concepts and assess simple scenarios |
| 2 | Manual web security testing | Test common web vulnerabilities in a local training application |
| 3 | API security testing | Design and automate API security tests |
| 4 | Security automation | Use DAST, SAST, SCA and secrets scanning tools |
| 5 | DevSecOps | Integrate security checks into GitHub Actions |
| 6 | AI-assisted security testing | Use AI to assist test design, triage and reporting with human validation |

See [`docs/learning-roadmap.md`](docs/learning-roadmap.md) for the detailed plan.

## Initial technology direction

- Learning references: OWASP Top 10, OWASP Web Security Testing Guide, PortSwigger Web Security Academy.
- Practice targets: OWASP Juice Shop and OWASP crAPI, run locally.
- API automation: Java, Maven, TestNG and REST Assured (introduced when appropriate).
- Security tooling: OWASP ZAP, Semgrep, OWASP Dependency-Check, Gitleaks and Trivy (introduced progressively).
- CI/CD: GitHub Actions.
- AI: introduced only after foundational understanding and repeatable checks exist.

Tool choices may evolve. Prefer free/open-source editions and verify licensing and feature limits before adopting a tool.

## Safety and authorised testing

Only test:
- Applications you own;
- Local intentionally vulnerable training applications; or
- Systems for which you have explicit, documented permission and a defined scope.

Do not scan public websites, employer systems, networks, APIs or cloud resources without explicit authorisation. Keep training targets local and isolated. Never commit passwords, API keys, tokens, personal data, or sensitive evidence.

See [`docs/testing-scope-and-safety.md`](docs/testing-scope-and-safety.md).

## Repository structure

```text
application-security-testing/
├── docs/
│   ├── architecture.md
│   ├── learning-journal.md
│   ├── learning-roadmap.md
│   ├── stage-1-security-fundamentals.md
│   └── testing-scope-and-safety.md
├── .gitignore
└── README.md
```

The repository will gain code, lab notes, test cases, reports and workflows as the learning progresses.

## Getting started

1. Read `docs/learning-roadmap.md`.
2. Read `docs/testing-scope-and-safety.md`.
3. Complete the first lesson and exercises in `docs/stage-1-security-fundamentals.md`.
4. Record your answers and reflections in `docs/learning-journal.md`.
5. Commit your work in small, meaningful changes.

## Free learning references

- [OWASP Top 10 (2025)](https://owasp.org/Top10/)
- [OWASP Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
- [OWASP crAPI](https://owasp.org/www-project-crapi/)

All resources listed here are free to access. Project and tool licences vary; check the official project pages before redistribution or commercial use.
