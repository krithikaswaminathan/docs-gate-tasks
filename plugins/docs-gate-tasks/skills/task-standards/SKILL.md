---
name: task-standards
description: Background knowledge for docs-gate-tasks — how to recognize a tutorial or an installation guide, and the checks each page type is reviewed against. Use when the review-task skill asks you to apply these checks, or when asked what docs-gate-tasks checks for.
---

> **Status: filled in.** [tutorial.md](tutorial.md) has checks T1–T14 and
> [install-guide.md](install-guide.md) has checks I1–I15, each with how to recognize the page
> type and credits for its sources.

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

Create a new file named for the type (for example `troubleshooting.md`) with the same structure
as `install-guide.md` — a "How to recognize" section and checks with the same four fields — fill it
in, add a row to the table above, and add the type to the list in
[review-task](../review-task/SKILL.md).
