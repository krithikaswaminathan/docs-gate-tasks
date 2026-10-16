---
title: Installing Tasklet
sidebar_label: Installing
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. SEEDED DEFECTS:
  I3  (Blocker): no system requirements anywhere.
  I5  (Nice-to-have): steps are prose paragraphs, unnumbered, with no expected results.
  I7  (Blocker): Windows is listed as supported, but has no steps.
  I8  (Blocker): no way to verify the installation.
  I10 (Blocker): no upgrade or downgrade information.
  I11 (Nice-to-have): no uninstall instructions.
  I12 (Blocker): no troubleshooting.
  I14 (Nice-to-have): no license.
Should pass: I1 (purpose and result), I2 (types listed), I4 (prerequisites), I6 (recommends the
script), I9 (says no configuration needed), I13 (next steps), I15 (version stated).
Expected review: needs work, 5 Blockers + 3 Nice-to-have. -->

# Installing Tasklet

Tasklet is a command-line tool for keeping to-do lists in your terminal. This page installs
Tasklet 2.4, so you can run the `tasklet` command from your terminal.

You can install Tasklet on macOS, Linux, or Windows, with either the install script or npm. We
recommend the install script.

## Before you begin

You'll need permission to install software in your user account. For npm, you'll also need
Node.js 20 or later.

## Install

On macOS or Linux, open a terminal and run
`curl -fsSL https://example.com/tasklet/install.sh | bash`, then open a new terminal. If you'd
rather use npm, run `npm install -g @example/tasklet@2.4` instead.

Tasklet doesn't need any configuration after it's installed.

## Next steps

- [Build your first to-do list with Tasklet](../tutorial/build-a-todo-cli.md)
