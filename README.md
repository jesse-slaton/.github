# .github

Default issue and pull request templates for jesse-slaton repositories.

GitHub uses the templates here for every jesse-slaton repository that has no `.github/ISSUE_TEMPLATE/` folder or pull request template of its own. A repository that defines its own replaces these entirely; it does not merge with them.

## Issue templates

| Template | Default label | Use for |
|---|---|---|
| `bug.md` | `bug` | Something is broken or behaves incorrectly |
| `feature.md` | `enhancement` | A new feature or an enhancement |
| `task.md` | `chore` | Refactor, cleanup, docs, CI, config or other non-feature work |

An issue template's default label is applied only if that label exists in the repository. `bug` and `enhancement` are GitHub's defaults; `chore` was created in every jesse-slaton repository alongside these templates, so create it in any new repository too. Keep `dependencies` free for Dependabot, which applies it to its own pull requests.

Each issue template opens with an agent-hints block. An agent working the issue uses exactly these settings, so set all three before submitting:

```
[mode: direct]   plan | direct
[model: sonnet]  fable | opus | sonnet | haiku
[effort: medium] low | medium | high | xhigh | max
```

## Pull request templates

- `pull_request_template.md` is the default.
- `PULL_REQUEST_TEMPLATE/chore.md` is for changes with no user-visible behavior change. Select it by adding `?template=chore.md` to the compare URL.

Both repeat the closing keyword for every linked issue: GitHub closes only the first issue in `Closes #1, #2`.
