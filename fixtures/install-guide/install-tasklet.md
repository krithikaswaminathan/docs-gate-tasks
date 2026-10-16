---
title: Install Tasklet
sidebar_label: Install
---

<!-- SYNTHETIC FIXTURE for docs-gate-tasks. "Tasklet" is a made-up product. This is the CLEAN
installation guide: it should pass I1-I15. See install-tasklet-defective.md for the seeded-defect
version. -->

# Install Tasklet

Tasklet is a command-line tool for keeping to-do lists in your terminal. This guide installs the
`tasklet` command on your computer. When you're done, you'll be able to run `tasklet` from any
terminal window.

This guide covers **Tasklet 2.4**. Tasklet is open source under the
[MIT License](https://github.com/example/tasklet/blob/main/LICENSE).

## Choose an installation type

| Installation type | Use it if |
| :--- | :--- |
| Install script (macOS and Linux) | You're on macOS or Linux. **Recommended for most readers.** |
| PowerShell script (Windows) | You're on Windows. |
| npm package | You already use Node.js and want to manage Tasklet with npm. |

## System requirements

| Installation type | Requirements |
| :--- | :--- |
| Install script | macOS 13 or later, or a 64-bit Linux distribution with glibc 2.31 or later; 50 MB of disk space |
| PowerShell script | Windows 11; PowerShell 7 or later; 50 MB of disk space |
| npm package | Any OS that runs Node.js 20 or later; 50 MB of disk space |

## Before you begin

- You need permission to install software in your user account. You don't need administrator
  access.
- For the npm package only: Node.js 20 or later and npm 10 or later. Check with `node --version`.

## Install with the install script (macOS and Linux)

1. In a terminal, run the install script:

   ```bash
   curl -fsSL https://example.com/tasklet/install.sh | bash
   ```

   You should see `Tasklet 2.4.0 installed to ~/.local/bin/tasklet`.

2. Open a new terminal window, so it picks up the new command. Running `which tasklet` there
   should print `~/.local/bin/tasklet`.

## Install with PowerShell (Windows)

1. In PowerShell, run the install script:

   ```powershell
   irm https://example.com/tasklet/install.ps1 | iex
   ```

   You should see `Tasklet 2.4.0 installed`.

2. Open a new PowerShell window, so it picks up the new command. Running `Get-Command tasklet`
   there should show the path to `tasklet.exe`.

## Install with npm

1. In a terminal, install the package globally:

   ```bash
   npm install -g @example/tasklet@2.4
   ```

   You should see `added 1 package` in the output.

## Verify the installation

In a new terminal window, run:

```bash
tasklet --version
```

You should see:

```text
tasklet 2.4.0
```

## Configure Tasklet

Tasklet works with its default settings. If you want to change them, these are the settings most
people adjust:

| Setting | Default | What it does |
| :--- | :--- | :--- |
| `data.path` | `~/.tasklet` | Where Tasklet stores your lists |
| `color` | `auto` | Whether output uses color: `auto`, `always`, or `never` |

Change a setting with `tasklet config set <setting> <value>`, for example
`tasklet config set color never`.

## Upgrade or downgrade

To upgrade, run the same install command again. The install scripts always install the latest
release; with npm, run `npm install -g @example/tasklet@latest`.

To go back to an earlier version, pass the version you want:

- Install script: `curl -fsSL https://example.com/tasklet/install.sh | bash -s -- --version 2.3.1`
- PowerShell: `& ([scriptblock]::Create((irm https://example.com/tasklet/install.ps1))) -Version 2.3.1`
- npm: `npm install -g @example/tasklet@2.3.1`

Your lists are kept when you upgrade or downgrade.

## Uninstall

Run:

```bash
tasklet self-uninstall
```

This removes the `tasklet` command. Your lists in `~/.tasklet` are kept; delete that folder too if
you want to remove them. If you installed with npm, run `npm uninstall -g @example/tasklet`
instead.

## Troubleshooting

| Problem | Cause | Fix |
| :--- | :--- | :--- |
| `tasklet: command not found` | The terminal was open before you installed. | Open a new terminal window. |
| `EACCES: permission denied` with npm | npm's global folder needs administrator access. | Set npm's prefix to a folder you own, or use the install script instead. |
| Script blocked on Windows | PowerShell's execution policy doesn't allow scripts. | Run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`, then try again. |

If none of these fixes it, open an issue at
[github.com/example/tasklet/issues](https://github.com/example/tasklet/issues).

## Next steps

- [Build your first to-do list with Tasklet](../tutorial/build-a-todo-cli.md)
