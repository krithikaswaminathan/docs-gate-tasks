---
title: Install Tasklet
sidebar_label: Install
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. No defects are seeded
yet: add them once install-guide.md's checks are written, so each one exercises a specific check. -->

# Install Tasklet

This page shows how to install the Tasklet CLI on macOS, Linux, and Windows.

## Requirements

- macOS 13 or later, a 64-bit Linux distribution, or Windows 11
- Node.js 20 or later

## Install

### macOS and Linux

```bash
curl -fsSL https://example.com/tasklet/install.sh | bash
```

### Windows

In PowerShell, run:

```powershell
irm https://example.com/tasklet/install.ps1 | iex
```

## Verify the installation

```bash
tasklet --version
```

You should see a version number that starts with `2.`.

## Uninstall

```bash
tasklet self-uninstall
```

## Next steps

- [Build your first to-do CLI](../tutorial/build-a-todo-cli.md)
