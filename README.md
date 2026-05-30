# FileCopyRenameTool

**File Copy & Rename Tool** — A lightweight Windows utility for intelligently copying files with smart conflict resolution.

![Main Window](screenshots/main-window.png)

## Overview

This tool helps you copy (or move) multiple files to a destination folder while avoiding common problems like accidental overwrites. It uses file size comparison to decide the best action when a file with the same name already exists.

## Features

- Select one or multiple source files at once
- Choose any destination folder
- Three intelligent copy behaviors:

  | Option | Behavior |
  |--------|----------|
  | **Skip if file with same name already exists and sizes are identical** | Skips the file completely if both name and size match (safe duplicate protection) |
  | **Auto-rename destination file when name already exists but size is different** | Automatically renames the new file (e.g. `file (1).txt`) when a name conflict exists but the content is different |
  | **Delete source file after successful copy** | Turns the operation into a **Move** instead of Copy |

- Simple and clean interface with clear status feedback

## How It Works (Logic)

The tool uses this decision process when a file with the same name exists in the destination:

1. If **"Skip if sizes are identical"** is enabled and sizes match → **Skip** the file
2. If sizes are **different** and **"Auto-rename"** is enabled → Copy with a new name (e.g. `filename (2).ext`)
3. If **"Move mode"** is enabled → Delete the original file after a successful copy

## How to Use

1. Run `FileCopyManager.exe`
2. Click **Select Source Files...** → Choose one or more files
3. Click **Select Destination...** → Choose the target folder
4. Configure the three options as needed (recommended defaults are usually the first two checkboxes enabled)
5. Click **Start Copy**

The tool will process the files according to your selected rules and show progress.

## Current Release

**Version 1.0** – March 2026

### Files Included

- `FileCopyManager.exe` (main application)
- Required .NET support files

## Requirements

- Windows 10 or Windows 11
- No installation required (portable .exe)

## Notes

- This is a compiled .NET application.
- The source code is not published in this repository yet.
- The executable name is still `FileCopyManager.exe` from the original build.

## Author

Created by **Orffyrus**

## Related Projects

- [LOGSEQ](https://github.com/Orffyrus-Qc/LOGSEQ) — Tools for making Logseq portable
- [GAME](https://github.com/Orffyrus-Qc/GAME) — Collection of game server tools and utilities

---

**Feedback & Contributions**

If you have ideas for improvements, found a bug, or would like the source code to be added, please open an issue.
