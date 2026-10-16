---
title: Build your first to-do list with Tasklet
sidebar_label: Build a to-do list
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. This is the CLEAN
tutorial: it should pass T1-T13. One goal (a to-do list you can add to and complete), beginner
level, tool and version named, finished output shown up front, final code linked, 7 reader actions,
throwaway folder, a checkpoint after each step, recap and next steps.
See too-much-tutorial.md and broken-promise-tutorial.md for the seeded-defect versions. -->

# Build your first to-do list with Tasklet

In this tutorial, you'll use the Tasklet command-line tool to build a to-do list in your terminal.
By the end, you'll be able to add a task, see your list, and mark a task as done.

**Who this is for:** beginners. You don't need to have used Tasklet before, but you should be able
to open a terminal and run a command.

**What you'll use:** Tasklet 2.4 and a terminal (any shell). It takes about 15 minutes.

Here's what your list will look like at the end:

```text
$ tasklet list
1  [x]  Buy milk
```

The finished project is at [github.com/example/tasklet-todo-tutorial](https://github.com/example/tasklet-todo-tutorial),
if you want to compare your work with it.

## Before you begin

- Install Tasklet 2.4. See [Install Tasklet](../install-guide/install-tasklet.md).

You'll work in a new, empty folder, so nothing in this tutorial touches your real task lists. You
can delete the folder when you're done.

## Step 1: Create a project

A Tasklet *project* is a folder that holds one to-do list. Create a folder and turn it into a
project:

```bash
mkdir todo-tutorial
cd todo-tutorial
tasklet init
```

`tasklet init` creates a file named `tasklet.json`, where Tasklet stores your tasks. You should see:

```text
Created tasklet.json
```

## Step 2: Add a task

Add your first task. The words in quotes are the task's name:

```bash
tasklet add "Buy milk"
```

Tasklet gives each task a number, which you'll use to refer to it later. You should see:

```text
Added task 1: Buy milk
```

## Step 3: See your list and finish a task

Show your list:

```bash
tasklet list
```

You should see your task, not yet done:

```text
1  [ ]  Buy milk
```

Now mark task 1 as done, using its number, and show the list again:

```bash
tasklet done 1
tasklet list
```

The `[x]` means the task is done:

```text
1  [x]  Buy milk
```

## What you learned

You created a Tasklet project, added a task to it, and marked the task as done. Those three
commands — `init`, `add`, and `done` — are the core of working with Tasklet.

## Next steps

- Read the [Tasklet command reference](https://example.com/tasklet/docs/commands) to see what else
  `tasklet list` can show.
