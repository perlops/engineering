
# PerlOps — Development Environment Standard

## 1. Purpose

This standard defines the development environment
for PerlOps software projects.

The objective is to provide consistent, reproducible,
secure, and portable development environments.

## 2. Supported Platforms

Primary development platforms:

- Linux
- Windows with WSL2
- macOS

Native Windows support may be provided depending
on project requirements.

## 3. Perl Runtime

- Initial minimum supported version: Perl 5.36.
- Prefer maintained stable Perl releases.
- Use Perlbrew or an equivalent version manager.
- Avoid modifying the operating system Perl installation.
- Document project-specific runtime requirements.

## 4. Development Toolchain

| Tool | Purpose |
|---|---|
| Git | Version control |
| Perlbrew | Perl version management |
| cpanminus | CPAN dependency installation |
| Carton | Reproducible dependency management |
| Perl::Tidy | Code formatting |
| Perl::Critic | Static analysis |
| Test2::V0 | Automated testing |
| Devel::Cover | Code coverage |
| Docker | Containerized environments |
| GitHub CLI | GitHub workflow automation |

## 5. Dependency Isolation

- Keep project dependencies isolated.
- Declare dependencies in a cpanfile.
- Use dependency snapshots where appropriate.
- Avoid unnecessary system-wide installations.
- Document required operating system packages.

## 6. Development Editors

Visual Studio Code is the recommended editor.

Developers may use alternative editors provided
that all engineering standards are respected.

Editor-specific configuration must not introduce
mandatory proprietary dependencies.

## 7. Environment Reproducibility

Projects should provide:

- Documented installation instructions.
- Dependency installation commands.
- Automated test execution commands.
- Example configuration files.
- Containerized development options where appropriate.

A new contributor should be able to prepare
a working environment with minimal manual effort.

## 8. Security Requirements

- Never store credentials in source code.
- Never commit local secrets.
- Use trusted software distribution sources.
- Keep development tools updated.
- Avoid unnecessary administrative privileges.
- Separate development and production credentials.
- Review third-party development tools and extensions.

## 9. Containerized Development

Docker may be used to provide isolated and
reproducible development environments.

Container images should:

- Use trusted base images.
- Minimize unnecessary packages.
- Run as non-root where practical.
- Avoid embedding credentials.
- Be versioned and regularly reviewed.

## 10. Local Quality Validation

Developers should validate changes locally before
submitting pull requests.

Validation should include:

- Perl syntax checks.
- Automated tests.
- Code formatting.
- Static analysis.
- Security checks where applicable.

## 11. CI/CD Alignment

Local development environments should remain
consistent with automated CI/CD environments.

Differences must be documented when necessary.

## 12. Standard Evolution

This standard will evolve as PerlOps projects
introduce new requirements and technologies.

---

**PerlOps — Automate. Secure. Modernize.**
