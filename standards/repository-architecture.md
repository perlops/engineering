
# PerlOps — Repository Architecture

## 1. Purpose

This standard defines a consistent repository structure
for software projects within the PerlOps ecosystem.

The objective is to improve maintainability, discoverability,
automation, security, and developer experience.

## 2. Repository Naming

Repository names must use lowercase kebab-case.

Examples:

- api-doctor
- modernize
- core
- log-intelligence
- compliance
- secrets
- gateway

## 3. Standard Repository Structure

```text
project-name/
├── .github/
│   ├── workflows/
│   ├── ISSUE_TEMPLATE/
│   └── pull_request_template.md
├── bin/
├── lib/
│   └── PerlOps/
├── t/
├── xt/
├── docs/
│   ├── architecture/
│   └── adr/
├── examples/
├── config/
├── share/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
├── cpanfile
├── Makefile.PL
├── .perltidyrc
├── .perlcriticrc
├── .gitignore
└── Dockerfile
```

## 4. Directory Responsibilities

| Directory | Responsibility |
|---|---|
| .github/ | CI/CD workflows and GitHub configuration |
| bin/ | Command-line entry points |
| lib/ | Perl modules and application logic |
| t/ | Automated functional and unit tests |
| xt/ | Extended and author-only tests |
| docs/ | Technical documentation |
| docs/architecture/ | Architecture documentation |
| docs/adr/ | Architecture Decision Records |
| examples/ | Practical usage examples |
| config/ | Example and default configurations |
| share/ | Application resources |

## 5. Required Files

Every public software repository must provide:

- README.md
- LICENSE
- CHANGELOG.md
- CONTRIBUTING.md
- SECURITY.md
- CODE_OF_CONDUCT.md
- .gitignore

Perl software repositories must additionally provide:

- cpanfile
- Makefile.PL
- .perltidyrc
- .perlcriticrc

## 6. Optional Components

Additional directories and files should be introduced
when required by the project.

Examples:

- Dockerfile
- compose.yaml
- config/
- share/
- xt/
- scripts/
- benchmarks/
- integrations/
- deploy/

Avoid unnecessary empty directories and infrastructure.

## 7. Module Namespaces

PerlOps modules should use a consistent namespace.

Examples:

- PerlOps::APIDoctor
- PerlOps::Modernize
- PerlOps::Core
- PerlOps::LogIntelligence
- PerlOps::Compliance

Public namespace availability must be verified before
publishing distributions to CPAN.

## 8. Separation of Responsibilities

- CLI interfaces must remain lightweight.
- Business logic must reside in reusable modules.
- Configuration must be separated from application logic.
- External integrations should use dedicated modules.
- Tests must not depend on production infrastructure.
- Generated artifacts must not be committed unnecessarily.

## 9. Configuration and Secrets

- Never commit credentials or sensitive configuration.
- Provide sanitized configuration examples.
- Support environment variables where appropriate.
- Exclude local secrets and runtime artifacts from Git.
- Document configuration requirements.

## 10. Repository Governance

Repositories should use:

- Protected default branches
- Pull requests
- Automated quality checks
- Documented release processes
- Semantic Versioning
- Conventional Commits
- Responsible vulnerability disclosure

## 11. Reusable Templates

Common repository components should be maintained
through reusable templates and shared workflows.

Project-specific exceptions must be documented.

## 12. Standard Evolution

This architecture represents the initial PerlOps baseline.

It will evolve through practical implementation and
documented engineering decisions.

---

**PerlOps — Automate. Secure. Modernize.**
