# Learning Project Architecture

## Architectural direction

This repository starts as a documentation-first learning project. It is deliberately not a full security framework on day one. The architecture will evolve as the learner understands the testing techniques and tools.

## Intended logical layers

```text
Learning and test strategy
        |
        v
Practice targets (local training applications)
        |
        +--> Manual testing and evidence
        |
        +--> API security tests (Java / REST Assured / TestNG)
        |
        +--> DAST (OWASP ZAP)
        |
        +--> SAST (Semgrep)
        |
        +--> SCA / secrets / container checks
        |
        v
GitHub Actions orchestration
        |
        v
Reports, triage, remediation and learning notes
        |
        v
AI-assisted test design and finding analysis (human reviewed)
```

## Design principles

1. **Safe by default:** use local intentionally vulnerable applications for practice.
2. **Modularity:** keep manual testing, API tests, scanners and CI orchestration independently understandable.
3. **Evidence before conclusions:** record request/response details, reproduction steps and tool output with secrets and personal data removed.
4. **Human validation:** scanner findings and AI suggestions require review.
5. **Reproducibility:** document prerequisites, versions, commands and configuration.
6. **Least privilege:** use dedicated lab accounts and minimal permissions.
7. **No secrets in Git:** use environment variables or GitHub Secrets when remote workflows are eventually introduced.
8. **Progressive complexity:** add tools only when there is a clear learning or testing objective.

## Planned repository evolution

The initial repository contains only documentation. Later additions may include:

```text
src/
  test/
    api/
    security/
security/
  zap/
  semgrep/
reports/
.github/
  workflows/
```

The final structure will be decided from actual use cases rather than created speculatively.
