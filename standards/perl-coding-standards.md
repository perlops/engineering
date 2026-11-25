
# PerlOps — Perl Coding Standards

## 1. Purpose

This document defines the coding standards for Perl software
developed within the PerlOps ecosystem.

The objective is to ensure consistency, readability, security,
maintainability, and reliability across all projects.

## 2. Perl Version

- Initial minimum supported version: Perl 5.36.
- Use maintained Perl versions whenever possible.
- Document compatibility requirements.
- Avoid deprecated and experimental features unless justified.

## 3. Language Fundamentals

All Perl modules and scripts must enable strict language checks.

Recommended baseline:

```perl
use v5.36;
use strict;
use warnings;
```

Prefer modern Perl features over outdated programming patterns.

## 4. Naming Conventions

| Element | Convention | Example |
|---|---|---|
| Variables | snake_case | `$api_response` |
| Functions | snake_case | `validate_payload()` |
| Modules | PascalCase | `PerlOps::API::Doctor` |
| Constants | UPPER_CASE | `DEFAULT_TIMEOUT` |
| CLI commands | kebab-case | `perlops-api-doctor` |

Names must be descriptive and meaningful.

## 5. Code Organization

- Separate business logic from CLI interfaces.
- Organize reusable functionality into modules.
- Avoid unnecessary global variables.
- Prefer small, focused functions.
- Use object-oriented programming where appropriate.
- Avoid duplicated logic.
- Favor composition over unnecessary inheritance.

## 6. Code Formatting

- Use four spaces for indentation.
- Avoid tabs.
- Prefer a maximum line length of 100 characters.
- Use Perl::Tidy for automated formatting.
- Use consistent whitespace and naming conventions.
- Remove trailing whitespace.

## 7. Static Analysis

Use Perl::Critic to identify potential issues and enforce
agreed coding practices.

Exceptions must be documented and justified.

## 8. Error Handling

- Validate external inputs.
- Handle expected failures explicitly.
- Provide meaningful error messages.
- Use appropriate process exit codes.
- Avoid silently ignoring errors.
- Do not expose sensitive information in error messages.

## 9. Security

- Never hardcode credentials or API keys.
- Never disable TLS verification by default.
- Validate and sanitize untrusted input.
- Avoid unsafe shell command execution.
- Apply the principle of least privilege.
- Review third-party dependencies.
- Redact sensitive information from logs and reports.

## 10. Logging

- Use consistent logging levels.
- Prefer structured logging where appropriate.
- Include relevant diagnostic context.
- Never log passwords, tokens, or private keys.
- Separate diagnostic output from machine-readable output.

## 11. Dependency Management

- Declare dependencies in a cpanfile.
- Document minimum dependency versions.
- Avoid unnecessary dependencies.
- Review dependency licenses.
- Maintain reproducible dependency installations.

## 12. Testing

- Use Test2::V0 for new projects.
- Store automated tests in the t/ directory.
- Test successful and unsuccessful execution paths.
- Include regression tests for bug fixes.
- Avoid requiring external production services during tests.
- Use Devel::Cover to measure code coverage.

## 13. Documentation

- Use English for code, comments, and documentation.
- Use POD for Perl module documentation.
- Document public interfaces and expected behavior.
- Include practical usage examples.
- Explain architectural decisions where necessary.

## 14. AI-Assisted Development

AI-generated code must be subject to the same engineering
standards as human-written code.

- Review generated code before integration.
- Validate correctness through automated tests.
- Review security implications.
- Never expose confidential information to unauthorized AI services.
- Maintain human accountability for engineering decisions.

## 15. Quality Gates

Before merging code, projects should verify:

- Syntax validation
- Automated tests
- Code formatting
- Static analysis
- Security checks
- Documentation updates where required

## 16. Standard Evolution

This standard will evolve through practical implementation,
technical reviews, and documented engineering decisions.

---

**PerlOps — Automate. Secure. Modernize.**
