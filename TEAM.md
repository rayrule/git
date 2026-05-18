# Team Machines

This repository is shared by three machines through GitHub SSH access.

## Machine Names

- `main-windows`: primary Windows machine. Owns coordination, final integration, and release decisions.
- `worker-desktop`: secondary desktop worker. Handles assigned implementation tasks.
- `worker-steamdeck`: Steam Deck worker. Checks assigned tasks, runs focused validation, and reports results.

## Collaboration Rules

1. Always run `git pull --ff-only` before starting work.
2. Check `TASKS.md` for assignments before editing files.
3. Only work on tasks assigned to your machine name unless explicitly redirected.
4. Commit small, clear changes.
5. Push after each completed task.
6. If a merge conflict appears, stop and report it instead of guessing.

