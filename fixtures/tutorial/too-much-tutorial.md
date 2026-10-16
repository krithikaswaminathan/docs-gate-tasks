---
title: Get started with Tasklet
sidebar_label: Get started
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. SEEDED DEFECTS —
this page fails almost everything up front:
  T1  (Blocker): mixes three goals (to-do list, team sync, reminders by email) with no single one stated.
  T2  (Should-fix): 14 reader actions, counting sub-steps.
  T3  (Should-fix): no practice environment; the steps run against the reader's real account and team.
  T4  (Blocker): no audience level stated.
  T5  (Blocker): no tools or versions named.
  T6  (Blocker): no finished result shown before the first step.
  T7  (Blocker): no link to final code.
  T10 (Blocker): no checkpoints after any step.
  T11 (Blocker): steps are bare commands with no explanation.
  T13 (Blocker): "You're all set." is not a recap and gives no next steps.
Not assessed: T8 (no goal stated, reported under T1), T12 (no level stated, reported under T4).
T9 is a judgment call here: the page has no single goal to drift from.
Expected review: needs work, 8 Blockers + 2 Should-fix. -->

# Get started with Tasklet

Tasklet does a lot. This page walks through it.

## Step 1: Set up a list

1. Open your terminal and go to your home folder.
2. Run `tasklet init`.
3. Run `tasklet add "Quarterly report"`.
4. Run `tasklet add "Book flights"`.

## Step 2: Sync with your team

1. Run `tasklet login` and sign in with your work account.
2. Run `tasklet team join engineering`.
3. Run `tasklet sync`.
4. Open `~/.tasklet/team.json` and set `"shareAll": true`.

## Step 3: Turn on email reminders

1. Run `tasklet config set email you@example.com`.
2. Run `tasklet remind 1 --at "tomorrow 9am"`.
3. Run `tasklet remind 2 --at "friday 5pm"`.
4. Run `tasklet config set digest daily`.

## Step 4: Check everything

1. Run `tasklet list --team`.
2. Run `tasklet status`.

You're all set.
