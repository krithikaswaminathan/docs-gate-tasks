# Tutorial checks

> **Source:** adapted from the section on tutorials in *Docs for Developers: An Engineer's Field
> Guide to Technical Writing* (Jared Bhatti, Zachary Sarah Corleissen, Jen Lambourne, David
> Nunez, and Heidi Waterhouse; Apress, 2021). Paraphrased; severities and scope are the author's
> own calls.
>
> Anything still marked `TODO` is a placeholder. `review-task` treats a check that still says
> `TODO` as not defined and doesn't apply it.

## How to recognize a tutorial

A tutorial is a procedure that teaches the reader how to reach one specific goal. It lets the
reader try something out, such as an integration, in a setting meant for learning, rather than
building the real thing. It may supply a practice environment, test data, or tools for that.

TODO: what tells a tutorial apart from an installation guide.

## Checks

### T1. One specific goal

- **What to look for**: what the reader will be able to do, or will have built, by the end of the
  tutorial.
- **Passes when**: the page works toward one specific goal, and a reader can tell what it is.
- **Severity if it fails**: **Blocker** — no clear goal, or several goals combined in one
  tutorial.
- **Doesn't apply when**: always applies.

### T2. Ten steps or fewer

- **What to look for**: the number of actions the reader has to take to finish. Count every
  action — each command run, setting changed, file edited, or button clicked — including actions
  inside a sub-step, not just numbered steps or step headings.
- **Passes when**: the tutorial has ten actions or fewer.
- **Severity if it fails**: **Should-fix** — a long tutorial makes it less likely the reader
  finishes. In the report, give the count, and suggest splitting the tutorial or narrowing its
  goal. If the steps can't be cut, suggest raising with the product's developers whether some
  of them could be combined, automated, or removed from the product itself.
- **Doesn't apply when**: always applies.

### T3. A place to learn

- **What to look for**: where the reader does the tutorial, and what they use to do it.
- **Passes when**: the page tells the reader what environment to work in (for example a sandbox,
  a test account, or a throwaway project), and supplies or points to any test data or tools the
  tutorial needs, so the reader can practice without touching real work or production systems.
- **Severity if it fails**: **Should-fix**.
- **Doesn't apply when**: always applies.
