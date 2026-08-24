# Security Policy

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues,
pull requests, or discussions.**

Instead, use one of:

- **GitHub private vulnerability reporting** — on the affected repository, go to
  the **Security** tab and choose **Report a vulnerability**. This is the
  preferred route; it keeps the report private until a fix ships.
- **Email** — `founders@simantic.dev`.

Please include as much of the following as you can:

- The repository, version, or commit affected.
- What kind of issue it is (for example: remote code execution, credential
  disclosure, path traversal, sandbox escape).
- Steps to reproduce, ideally a minimal proof of concept.
- The impact you believe it has, and any configuration required to trigger it.

## What to expect

- We aim to acknowledge a report within **3 business days**.
- We will keep you updated as we confirm and work on a fix.
- We will let you know when a fix is released, and we are happy to credit you
  in the release notes — tell us how you would like to be named, or if you
  would rather stay anonymous.

We ask that you give us a reasonable opportunity to ship a fix before
disclosing publicly.

## Scope

This policy covers the repositories published under
[github.com/simantic-dev](https://github.com/simantic-dev) and the
`simantic` package on PyPI.

Reports about the hosted service at `simantic.dev` are also welcome at the
same addresses.

Some of our public repositories are forks of upstream projects (for example
`qemu`). If the issue is in upstream code and not in our changes, please
report it to the upstream project so their users are covered too — and feel
free to let us know as well.

## Supported versions

Simantic is in alpha. We ship fixes on the latest release only; there are no
long-term support branches yet.
