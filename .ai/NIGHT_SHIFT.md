# NIGHT SHIFT

1. Read `AGENTS.md`, `.ai/PROJECT_BOARD.md`, `.ai/LEASE.md`, README/WORKFLOW/SKILL and task-relevant references.
2. `git fetch origin`; use `origin/codex/night-shift` as durable checkpoint; never force.
3. Acquire lease; if another unexpired ACTIVE run owns it, exit.
4. Resume RUNNING, otherwise highest READY.
5. Work in small milestones: inspect → change → verify → update board/lease → commit → push `codex/night-shift`.
6. Preserve scientific provenance and do not change conclusion-affecting methods without approval.
7. Missing real microscopy data goes to BLOCKED; continue safe documentation/tooling/test work.
8. Do not invent new analysis scope merely to consume quota.
9. Normal end releases lease; hard interruption may leave ACTIVE until TTL takeover.