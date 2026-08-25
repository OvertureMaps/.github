# Pull Request Checks <!-- omit in toc -->

Standard automated PR checks run across all OvertureMaps repositories to keep contributions consistent, linked to tracked work, and free from indefinitely stale PRs. Each check posts a clear failure message with instructions.

In addition to the workflow checks below, all PRs also require a passing [DCO check](#developer-certificate-of-origin-sign-off) enforced by the CNCF DCO GitHub App.

- [How-to](#how-to)
- [Reference](#reference)
- [Explanation](#explanation)

## How-to

### Fix a failing PR title check

Edit the PR title to match one of the formats in [PR title format](#pr-title-format) below. If your repo requires **Overture PR Checks (v2)**, only `type: description` is accepted; if it requires the original **Overture PR Checks**, all formats below are accepted. The comment posted on the PR clears automatically once the title passes.

To skip the check for automated or exceptional PRs, add a `bot` or `ignore-semantic-pull-request` label.

### Link an issue to a PR

- Same repo: add `Fixes #123`, `Closes #123`, or `Resolves #123` to the PR body, or use the Development panel in the PR sidebar
- Cross-repo: use `Fixes OvertureMaps/schema#123` in the PR body, or link from the Development panel on the issue itself (the PR sidebar only supports same-repo links)

After linking, re-run the check manually from the Checks tab if it does not trigger automatically.

### Reset a stale PR

Leave a comment, push a commit, or remove the `stale` label. Any of these reset the inactivity clock.

## Reference

### PR title format

```text
type: Short description of the change
type(scope): Short description of the change
type(scope)!: Short description of the change

[TYPE] Short description of the change
[TYPE](scope) Short description of the change
[BREAKING][TYPE] Short description of the change
```

The optional `(scope)` narrows the area of the codebase affected (e.g. `refactor(schema): consolidate validation logic`). A `!` before the colon (or a `[BREAKING]` prefix) marks a breaking change (e.g. `feat(api)!: remove deprecated endpoint`).

Use `[WIP]` as a prefix on repos without draft PR support.

| Conventional Commits type | Legacy equivalent | Use for |
|---|---|---|
| `fix` | `BUG`, `SECURITY` | Fixing a defect (including security fixes, e.g. `fix(security): sanitize user input`) |
| `feat` | `FEATURE`, `ENHANCEMENT` | Adding new functionality or improving existing functionality |
| `docs` | `DOCS` | Documentation-only changes |
| `refactor` | `REFACTOR` | Code restructuring without behavior change |
| `test` | `TEST` | Adding or updating tests |
| `chore` | `CHORE` | Maintenance, dependency updates, tooling |
| `perf` | `PERFORMANCE` | Performance improvements |

`INVESTIGATION` has no Conventional Commits equivalent and isn't accepted by either workflow — exploratory or spike work shouldn't typically result in PRs.

Overture offers two reusable PR title workflows a repo can require:

- **Overture PR Checks** (original) — accepts every row above: both syntaxes and both the Conventional Commits and legacy type words.
- **Overture PR Checks (v2)** — accepts only the Conventional Commits column and the `type:` syntax.

Since this check runs as an org-required workflow, individual repos have no toggleable input to control it — the mechanism is choosing which named workflow to require. A repo's maintainers switch from **Overture PR Checks** to **Overture PR Checks (v2)** whenever that repo is ready to fully migrate — see the [maintainer guide](https://github.com/OvertureMaps/operating-procedures/blob/main/development/pr-checks-maintainer.md) for how to set it.

### Staleness thresholds

| Stage | Default |
|---|---|
| `stale` label applied | 30 days of inactivity |
| PR closed | 14 days after stale label |

Closing a stale PR does not delete the branch. Branch deletion only fires on merges, via Settings -> General -> "Automatically delete head branches".

## Explanation

### Why these checks exist

Overture has contributors across many repos and organizations. Without consistent standards, PR titles become opaque to reviewers, contributions lose their link to tracked work, and long-open PRs accumulate without anyone knowing their status. These checks enforce a small set of conventions at the point of contribution, where the cost of correction is lowest.

### Why title format matters

A consistent title format makes changelogs, release notes, and search useful without manual categorization. The `type` prefix is machine-readable and gives reviewers immediate context when triaging a queue of open PRs. Since this check runs as an org-required workflow with no per-repo input to flip, offering **Overture PR Checks (v2)** as a discrete workflow (which also accomplishes other, unrelated improvements) alongside the original **Overture PR Checks** lets each repo's maintainers switch whenever their contributors are ready, rather than forcing every repo onto one org-wide deadline. Bracket syntax and legacy type words stay supported indefinitely under the original Overture PR Checks.

### Why linked issues are required

A PR without a linked issue leaves reviewers without the "why". Issues are where intent, discussion, and acceptance criteria live. Requiring a link ensures that even if a contributor is familiar with the work, the connection is explicit for anyone who encounters the PR later.

### Why issues are not subject to staleness

Issue staleness is a product and triage concern, not a contribution hygiene concern. Automatically closing issues would risk losing valid long-lived feature requests or bug reports. The staleness policy is scoped to PRs only, where an unmerged and unattended contribution represents concrete pending review work.

### Developer Certificate of Origin sign-off

Every commit must include a `Signed-off-by` line certifying that you have the right to submit the contribution under the project's license. Add it with:

```
git commit -s
```

or manually append to your commit message:

```
Signed-off-by: Your Name <your@email.com>
```

The name and email must match your git `user.name` and `user.email` configuration. If a commit is missing the sign-off, the DCO check will fail and block merging.

See [dco-guidelines.md](https://github.com/OvertureMaps/.github/blob/main/docs/dco-guidelines.md) for background on the DCO.

---

Repo maintainers: see the [PR checks maintainer guide](https://github.com/OvertureMaps/operating-procedures/blob/main/development/pr-checks-maintainer.md) for setup, configuration, and customization.
