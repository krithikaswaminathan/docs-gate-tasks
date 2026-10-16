---
title: Build your first to-do CLI
sidebar_label: Build a to-do CLI
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. This is the CLEAN
tutorial: it should pass T1-T3 (one goal, 7 actions, practice folder stated). See
too-much-tutorial.md for the seeded-defect version. -->

# Build your first to-do CLI

In this tutorial, you'll use Tasklet to build a small command-line to-do list. By the end, you'll
be able to add, list, and complete tasks from your terminal.

This tutorial is for developers who are new to Tasklet. It takes about 15 minutes.

## Before you begin

- Tasklet 2.x installed. See [Install Tasklet](../install-guide/install-tasklet.md).
- A terminal.

You'll work in a new, empty folder, so nothing in this tutorial touches your real task lists. You
can delete the folder when you're done.

## Step 1: Create a project

Create a new folder and start a Tasklet project in it:

```bash
mkdir todo-cli && cd todo-cli
tasklet init
```

Tasklet creates a `tasklet.json` file in the folder.

## Step 2: Add a task

Add your first task:

```bash
tasklet add "Buy milk"
```

You should see:

```text
Added task 1: Buy milk
```

## Step 3: List and complete tasks

List your tasks, then mark the first one done:

```bash
tasklet list
tasklet done 1
```

Run `tasklet list` again. Task 1 now shows as complete.

## What you built

You created a Tasklet project, added a task, and completed it.
