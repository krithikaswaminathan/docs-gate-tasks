# Tutorial checks

> **Sources** (paraphrased; severities and scope are the author's own calls):
> - **T1–T3:** the section on tutorials in *Docs for Developers: An Engineer's Field Guide to
>   Technical Writing* (Jared Bhatti, Zachary Sarah Corleissen, Jen Lambourne, David Nunez, and
>   Heidi Waterhouse; Apress, 2021).
> - **T4–T13:** David Colby, ["Writing effective coding tutorials"](https://www.colby.so/posts/writing-effective-coding-tutorials)
>   (July 2022).
> - **How to recognize a tutorial (second paragraph) and T14:** Diátaxis,
>   ["The difference between a tutorial and how-to guide"](https://diataxis.fr/tutorials-how-to/).
>
> Anything still marked `TODO` is a placeholder. `review-task` treats a check that still says
> `TODO` as not defined and doesn't apply it.

## How to recognize a tutorial

A tutorial is a procedure that teaches the reader how to reach one specific goal. It lets the
reader try something out, such as an integration, in a setting meant for learning, rather than
building the real thing. It may supply a practice environment, test data, or tools for that.

A tutorial is for a reader who is learning: it follows one path with no branches, and is safe to
repeat. An installation guide is a how-to guide for a reader with a job to do (getting the software
installed): it may branch by operating system or setup, and assumes the reader can handle
surprises. Whether the material is basic or advanced doesn't decide the type. (Source: Diátaxis.)

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

### T4. One audience level, stated

- **What to look for**: the experience level the tutorial is written for (for example beginner,
  intermediate, or advanced), stated in the introduction.
- **Passes when**: the introduction names one level, and the rest of the page is written for that
  reader rather than trying to serve every level at once.
- **Severity if it fails**: **Blocker** — no level stated, or the page mixes levels (for example
  explaining basic setup alongside advanced techniques).
- **Doesn't apply when**: always applies.

### T5. Tools and versions named

- **What to look for**: the tools, languages, frameworks, or products the tutorial uses, and their
  versions.
- **Passes when**: the introduction names each tool the reader needs and the version the tutorial
  was written against.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### T6. Finished result shown up front

- **What to look for**: a preview of what the reader will end up with, near the start of the page.
- **Passes when**: before the first step, the page shows the finished result — a screenshot, an
  animation, or, for a project with nothing visual, sample output such as terminal output, logs,
  or an API response.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### T7. Link to the final code

- **What to look for**: a link to the finished code, for example a repository or a downloadable
  project.
- **Passes when**: the page links to the complete code the tutorial builds, so the reader can
  compare it with their own.
- **Severity if it fails**: **Should-fix**.
- **Doesn't apply when**: the tutorial doesn't produce any code.

### T8. Delivers what it promised

- **What to look for**: the goal stated near the start (see T1), compared with what the reader
  actually has at the end.
- **Passes when**: by the end of the page, the reader has built or done what the introduction said
  they would, with the tools it said they'd use.
- **Severity if it fails**: **Blocker** — the page stops short of the stated goal, or delivers
  something different.
- **Doesn't apply when**: T1 fails because no goal is stated; report it under T1 instead.

### T9. Stays on topic

- **What to look for**: setup, features, or techniques that don't serve the tutorial's goal.
- **Passes when**: everything on the page serves the goal. Setup the lesson doesn't depend on is
  cut or moved elsewhere (for example a starter repository the reader can begin from), and the
  page doesn't add unrelated features or show off techniques beside the main topic.
- **Severity if it fails**: **Blocker**. In the report, name the section that drifts and what it
  drifts into.
- **Doesn't apply when**: always applies.

### T10. Checkpoints after major sections

- **What to look for**: what the reader should see after each major section or milestone.
- **Passes when**: after each major section, the page shows the expected result — a screenshot,
  terminal output, logs, or an API response — so the reader can confirm they're on track before
  moving on.
- **Severity if it fails**: **Blocker**. In the report, list the sections without a checkpoint.
- **Doesn't apply when**: always applies.

### T11. Built step by step, with each step explained

- **What to look for**: how the work is broken up, and whether each piece is explained.
- **Passes when**: the work is built up in a sequence of steps (for code, in increments rather than
  one finished block), and each step says what it does and why, so the reader learns rather than
  copies.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: always applies.

### T12. Explanation fits the audience

- **What to look for**: how much the page explains, compared with the level stated under T4.
- **Passes when**: for beginners, the page explains in more detail, slows down for complex code,
  avoids or defines jargon, and links to further reading. For advanced readers, it skips the
  basics, says briefly what it assumes, and links to reference docs for anyone who needs a
  refresher. At any level, concepts that aren't central to the lesson get only a brief mention.
- **Severity if it fails**: **Blocker**.
- **Doesn't apply when**: T4 fails because no level is stated; report it under T4 instead.

### T13. Recap and next steps

- **What to look for**: a closing section.
- **Passes when**: the page ends by recapping what the reader learned or built, and points to what
  to read or try next.
- **Severity if it fails**: **Should-fix**.
- **Doesn't apply when**: always applies.

### T14. One path, no branches

- **What to look for**: conditional steps ("if you're on Windows, do this instead"), optional
  steps, or alternative ways to do the same thing.
- **Passes when**: the tutorial follows one path from start to finish, with no branches or
  alternatives for the reader to choose between.
- **Severity if it fails**: **Nice-to-have**. In the report, suggest picking one path for the
  tutorial and moving the alternatives to a how-to guide.
- **Doesn't apply when**: always applies.
