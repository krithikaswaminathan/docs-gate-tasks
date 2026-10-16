---
name: task-standards
description: Background knowledge for docs-gate-tasks — how to recognize a tutorial or an installation guide, and the checks each page type is reviewed against. Use when the review-task skill asks you to apply these checks, or when asked what docs-gate-tasks checks for.
---

> **Status: in progress.** [tutorial.md](tutorial.md) is filled in: how to recognize a tutorial,
> and checks T1–T14. [install-guide.md](install-guide.md) is still an
> empty template. Until a file's checks are written, `review-task` reports that the checks for
> that page type aren't defined yet instead of inventing its own.

# task-standards

The shared standard `review-task` applies. It holds no logic of its own — it's reference
material, loaded on demand rather than kept in context every turn.

## Reference files

| File | Holds |
| :--- | :--- |
| [severity.md](severity.md) | The three severities every finding uses |
| [tutorial.md](tutorial.md) | How to recognize a tutorial, and the checks for one |
| [install-guide.md](install-guide.md) | How to recognize an installation guide, and the checks for one |

Read only the file for the page type under review, plus `severity.md`.

## Adding another page type

Copy `install-guide.md` to a new file named for the type (for example `troubleshooting.md`), fill
it in, add a row to the table above, and add the type to the list in
[review-task](../review-task/SKILL.md).
