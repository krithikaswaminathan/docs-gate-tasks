---
title: Build a Tasklet dashboard in your browser
sidebar_label: Build a dashboard
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. SEEDED DEFECTS — this
page passes the "up front" checks (goal, level, tools, preview, final code, practice folder, step
count) so that the checks which depend on a stated goal and level can fire:
  T8  (Blocker): promises a browser dashboard; the page ends with terminal output only.
  T9  (Blocker): Step 2 drifts into tuning the sync cache, which the goal doesn't need.
  T10 (Blocker): Step 2 and Step 3 have no checkpoint.
  T11 (Blocker): Step 3 hands over a finished config block with no explanation.
  T12 (Blocker): written for beginners, but uses undefined jargon ("idempotent", "TTL",
                 "hydrate") and explains nothing.
  T13 (Should-fix): no recap or next steps.
  T14 (Nice-to-have): Step 1 branches for Windows readers.
Expected review: needs work, 5 Blockers + 1 Should-fix + 1 Nice-to-have. T1-T7 should pass. -->

# Build a Tasklet dashboard in your browser

In this tutorial, you'll build a web dashboard that shows your Tasklet tasks in your browser.

**Who this is for:** beginners who have used the Tasklet command line but haven't built anything
with it.

**What you'll use:** Tasklet 2.4 and a web browser.

Here's the dashboard you'll build:

![A browser window showing three Tasklet tasks in a table](./images/dashboard.png)

The finished project is at [github.com/example/tasklet-dashboard](https://github.com/example/tasklet-dashboard).

## Before you begin

Work in a new, empty folder so nothing touches your real task lists.

## Step 1: Create a project

```bash
mkdir dashboard-tutorial
cd dashboard-tutorial
tasklet init
```

If you're on Windows, run `md dashboard-tutorial` instead of `mkdir dashboard-tutorial`.

You should see:

```text
Created tasklet.json
```

## Step 2: Tune the sync cache

Tasklet's sync is idempotent, but the default cache TTL is conservative. Before going further,
lower it so hydrate calls return faster:

```bash
tasklet config set cache.ttl 5
tasklet config set cache.prefetch true
```

## Step 3: Configure the dashboard

Paste this into `tasklet.json`:

```json
{
  "dashboard": {
    "enabled": true,
    "port": 4100,
    "columns": ["id", "title", "status"],
    "hydrate": "eager"
  }
}
```

## Step 4: Check it

```bash
tasklet list
```

```text
1  [ ]  Buy milk
```
