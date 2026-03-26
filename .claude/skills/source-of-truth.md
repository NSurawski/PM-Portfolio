---
name: source-of-truth
description: Track which files are copies vs sources to prevent sync issues
autoInvoke:
  - pattern: "todo-prioritizer.html"
  - pattern: "meeting-summarizer.html"
  - keyword: "sync"
  - keyword: "copy"
  - keyword: "demo"
---

# Source of Truth for Demo Apps

Some files in this portfolio repo are **copies** of apps maintained in separate project directories. Edits should be made to the source, then synced here.

## File origins

| Portfolio file | Source of truth | Notes |
|---|---|---|
| `todo-prioritizer.html` | `/Users/nicolesurawski/Documents/PM projects/todo-prioritizer/todo-prioritizer.html` | Direct copy |
| `meeting-summarizer.html` | Simplified standalone version of the Vite app in `/Users/nicolesurawski/Documents/PM projects/meeting-summarizer/` | Not a direct copy — standalone demo version |
| `pm-toolkit.html` | Check if standalone or has a separate project | May be standalone |
| `collab-focus-mode.html` | Check if standalone or has a separate project | May be standalone |

## Rules
1. **Never edit demo app copies directly** in this repo if a source project exists — edit the source project instead
2. After updating a source project, **sync the copy** to this portfolio repo
3. If you're unsure whether a file is a copy, check for a matching project in `/Users/nicolesurawski/Documents/PM projects/`
4. PRD pages, case studies, teardowns, metrics, and research pages are **original to this repo** — edit them directly
