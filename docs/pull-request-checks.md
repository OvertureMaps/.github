# Pull Request Checks <!-- omit in toc -->

Standard automated PR checks run across all OvertureMaps repositories to keep contributions consistent, linked to tracked work, and free from indefinitely stale PRs. Each check posts a clear failure message with instructions.

In addition to the workflow checks below, all PRs also require a passing [DCO check](#developer-certificate-of-origin-sign-off) enforced by the CNCF DCO GitHub App.

- [How-to](#how-to)
- [Reference](#reference)
- [Explanation](#explanation)

## How-to

### Fix a failing PR title check

Edit the PR title to match `[TYPE] Description`. The comment posted on the PR clears automatically once the title passes.

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
[TYPE] Short description of the change
[TYPE](scope) Short description of the change
[BREAKING][TYPE] Short description of the change
```

The optional `(scope)` narrows the area of the codebase affected (e.g. `[REFACTOR](schema) Consolidate validation logic`).

Use `[WIP]` as a prefix on repos without draft PR support.

| Type | Use for |
|---|---|
| `BUG` | Fixing a defect |
| `FEATURE` | Adding new functionality |
| `ENHANCEMENT` | Improving existing functionality |
| `DOCS` | Documentation-only changes |
| `REFACTOR` | Code restructuring without behaviour change |
| `TEST` | Adding or updating tests |
| `CHORE` | Maintenance, dependency updates, tooling |
| `PERFORMANCE` | Performance improvements |
| `SECURITY` | Security fixes or hardening |
| `INVESTIGATION` | Exploratory or spike work |

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

A consistent title format makes changelogs, release notes, and search useful without manual categorization. The `[TYPE]` prefix is machine-readable and gives reviewers immediate context when triaging a queue of open PRs.

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
