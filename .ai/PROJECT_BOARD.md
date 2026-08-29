# PROJECT BOARD — microscopy-fluorescence-workflow

## MODE
`SCIENTIFIC_MAINTENANCE`

## STATE
- Reusable red-fluorescence microscopy analysis workflow covering Leica files, image organization, ImageJ mean fluorescence, Excel/Prism formatting, image/data/PPT consistency, and decision boundaries.
- Includes a Codex skill and detailed references.

## QUEUE
### MFW-P0-001 — Workflow/skill/reference consistency audit
- status: READY
- goal: Check README, WORKFLOW, SKILL and decision-boundary references for contradictions, stale paths or ambiguous channel/provenance rules; fix documentation drift only.

### MFW-P0-002 — Reproducibility contract audit
- status: READY
- goal: Verify the workflow explicitly protects source images, grouping labels, channel mapping, exclusion rules and output traceability; add non-destructive validation/checklist material where gaps are clear.

### MFW-P1-001 — Synthetic fixture/test plan
- status: READY
- goal: Add or document synthetic-only fixtures/tests for scripts or file-contract logic where useful, without pretending they validate real microscopy measurements.

### MFW-P1-002 — Packaging/install audit
- status: READY
- goal: Verify the skill can be copied/installed and invoked as documented; fix path/readme drift.

## IDEA INBOX
New quantification methods, segmentation, colocalization, threshold algorithms or scientific metrics are ideas unless explicitly approved.

## BLOCKED
- Real image analysis/quantification requires actual source files and confirmed experiment/channel/group context.
- Any change that could alter scientific conclusions needs user review.

## LAST CHECKPOINT
ChatGPT PM initialized Night Shift maintenance mode on 2026-08-30.