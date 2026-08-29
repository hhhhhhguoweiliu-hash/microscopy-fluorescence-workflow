# AGENTS.md — Microscopy Fluorescence Workflow AI Rules

This repository is a scientific image-analysis workflow/skill. User owns scientific decisions; ChatGPT PM coordinates; Codex may maintain the workflow, docs, scripts/tests, and reproducibility in low-risk reversible scope.

Before work read `README.md`, `WORKFLOW.md`, `skills/microscopy-fluorescence-workflow/SKILL.md`, `.ai/PROJECT_BOARD.md`, `.ai/NIGHT_SHIFT.md`, `.ai/LEASE.md`, and relevant references.

Scientific boundary:
- Do not invent measurements, image provenance, channel identities, exclusions, thresholds, or experimental conclusions.
- Do not silently change analysis rules that could alter scientific conclusions.
- If source images/data are absent, improve tooling/specification/tests with synthetic fixtures only and label them synthetic.
- New analysis methods belong in IDEA INBOX until clearly approved.

Safe maintenance can proceed autonomously: consistency checks, docs fixes, non-destructive tooling, synthetic tests, file-contract validation.

Stable milestones: verify, update board/lease, commit, push `codex/night-shift`; never force or auto-merge main.