# Task Board

This file is the fixed task entrypoint for all machines.

## Status Values

- `todo`: not started
- `doing`: currently being worked on
- `blocked`: waiting for input or a dependency
- `done`: completed and pushed

## Current Assignments

| ID | Owner | Status | Task | Notes |
| --- | --- | --- | --- | --- |
| T001 | `worker-steamdeck` | `done` | Verify repository access from Steam Deck | Run `git pull --ff-only`, then confirm the latest `TASKS.md` is visible. |
| T002 | `main-windows` | `todo` | Assign the first real project task | Add the first implementation or validation task here. |
| T003 | `worker-desktop` | `todo` | Verify repository access from worker desktop | Run `git pull --ff-only`, then confirm the latest `TASKS.md` is visible. |

## Reporting Format

When a machine reports back, include:

- Machine name
- Task ID
- Commands run
- Result
- Blockers, if any
