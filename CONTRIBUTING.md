# Contributing Guidelines<!-- omit in toc -->

Thank you for your interest in contributing! Please take a moment to review these guidelines before getting started.

## Table of Contents<!-- omit in toc -->

- [Code of Conduct](#code-of-conduct)
- [Coding Standards](#coding-standards)
- [Developer Certificate of Origin](#developer-certificate-of-origin)
- [AI Use in Development](#ai-use-in-development)

---

## Code of Conduct

This project adheres to a [Code of Conduct](CODE-OF-CONDUCT.md). By participating, you are expected to uphold this standard. Please report unacceptable behavior to the maintainers.

## Coding Standards

- Follow the style conventions of the language, framework, and repository for the project.
- Run linters and formatters before committing (see project `README.md` for tooling).

---

## Developer Certificate of Origin

The DCO2 project uses a [Developers Certificate of Origin (DCO)](https://developercertificate.org/) to sign-off that you have the right to contribute the code being contributed. The full text of the DCO reads:

```text
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
1 Letterman Drive
Suite D4700
San Francisco, CA, 94129

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.


Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

Every commit needs to have signoff added to it with a message like:

```text
Signed-off-by: Joe Smith <joe.smith@example.com>
```

Git makes doing this fairly straight forward. First, please use your real name (sorry, no pseudonyms or anonymous contributions).

If you set your `user.name` and `user.email` in your git configuration, you can sign your commit automatically with `git commit -s` or `git commit --signoff`.

Signed commits in the git log will look something like:

```text
Author: Joe Smith <joe.smith@example.com>
Date:   Thu Feb 2 11:41:15 2018 -0800

    Update README

    Signed-off-by: Joe Smith <joe.smith@example.com>
```

Notice how the `Author` and `Signed-off-by` lines match. If they do not match the PR will be rejected by the automated DCO check.

If more than one person contributed to a commit than there can be more than one `Signed-off-by` line where each line is a signoff from a different person who contributed to the commit.

## AI Use in Development

This section describes our policies around using AI tools when contributing to this project.

### AI-Assisted Development

> **[PLACEHOLDER]** Describe the project's stance on using AI coding assistants (e.g., GitHub Copilot, Cursor, ChatGPT) during development. Address:
>
> - Which tools are permitted or recommended
> - Expectations around reviewing and validating AI-generated code
> - Any licensing or intellectual property considerations
> - Whether AI use should be disclosed in commits or pull requests

### AI-Generated Issues

> **[PLACEHOLDER]** Describe expectations when AI tools are used to draft or generate issues. Address:
>
> - Whether AI-generated issues are acceptable and under what conditions
> - Required human review before submission
> - How to label or disclose AI-drafted content
> - Quality standards that must be met regardless of how an issue was created

### AI-Generated Pull Requests

> **[PLACEHOLDER]** Describe the policy for pull requests that are substantially authored by AI agents or assistants. Address:
>
> - Whether AI-generated pull requests are accepted (e.g., via GitHub Copilot coding agent)
> - Required human review and accountability standards
> - How to label or disclose AI-generated contributions
> - Any additional scrutiny or testing requirements for AI-generated code
