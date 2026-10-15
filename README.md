# docs-gate-tasks

A Claude Code plugin that reviews **tutorials** and **installation guides** in docs-as-code repos
(Docusaurus, Mintlify) against checks written for each page type. It reviews and reports — it
never edits the pages it looks at.

It's a companion to [docs-gate](https://github.com/krithikaswaminathan/docs-gate), which applies a
general rubric to any docs page, but it stands alone: you don't need docs-gate installed.

> **Status: the checks aren't written yet.** The plugin's structure is in place, but the
> tutorial and installation-guide checks are empty templates. Until they're filled in, a review
> reports that no checks are defined for the page type.

## What it does

| Component | What it is | Read-only? |
|---|---|---|
| `/docs-gate-tasks:review-task <path> [type]` | Reviews one tutorial or installation guide against that type's checks: severity, check, location, evidence, suggested fix. `type` is `tutorial` or `install-guide`; leave it out to have the page type recognized | Yes |
| `task-standards` (skill) | How to recognize each page type, the checks for it, and the severity model | N/A (no logic) |

## Install

```bash
claude plugin marketplace add https://github.com/krithikaswaminathan/docs-gate-tasks
claude plugin install docs-gate-tasks@docs-gate-tasks-marketplace
```

**Try it without installing**, from this repo's root:

```bash
claude --plugin-dir ./plugins/docs-gate-tasks
```

Then, for example:

```
/docs-gate-tasks:review-task fixtures/tutorial/build-a-todo-cli.md tutorial
```

**Uninstall:**

```bash
claude plugin uninstall docs-gate-tasks@docs-gate-tasks-marketplace
claude plugin marketplace remove docs-gate-tasks-marketplace
```

## Writing the checks

The checks live in `plugins/docs-gate-tasks/skills/task-standards/`:

- `tutorial.md` — how to recognize a tutorial, and its checks (`T1`, `T2`, …)
- `install-guide.md` — how to recognize an installation guide, and its checks (`I1`, `I2`, …)

Each check has the same fields: what to look for, when it passes, its severity if it fails, and
when it doesn't apply. A check that still says `TODO` is skipped.

To add another page type, copy `install-guide.md`, fill it in, and list the new type in
`task-standards/SKILL.md` and `review-task/SKILL.md`.

## Fixtures

`fixtures/` holds synthetic pages about a made-up product, Tasklet. They don't have seeded
defects yet; add them once the checks exist, so each defect exercises a specific check.

## Design decisions

TODO

## What I learned

TODO

## License

MIT
