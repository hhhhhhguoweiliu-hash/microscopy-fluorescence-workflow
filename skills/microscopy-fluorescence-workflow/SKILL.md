---
name: microscopy-fluorescence-workflow
description: Standardize microscopy fluorescence workflows from LIF/TIFF inventory through image naming, magnification separation, ImageJ batch mean-intensity measurement, Prism-ready tables, and PowerPoint image panels. Use when working with Leica exports, ICC images, fluorescence channels, experimental groups encoded in image numbers or filenames, outlier/exclusion marks, Prism Column/Grouped data, or slide decks that must match quantified image fields.
---

# Microscopy Fluorescence Workflow

## Core rule

Preserve traceability from every reported number to one image field and from every slide image back to the same source field. Never silently switch image source, channel, threshold export, magnification, or selection rule.

Read [references/workflow.md](references/workflow.md) for the end-to-end procedure. Read [references/decision-boundaries.md](references/decision-boundaries.md) before any destructive operation, experimental interpretation, outlier decision, threshold choice, or full-deck generation.

## Required sequence

1. Inventory source files and record exact folders, extensions, channel suffixes, image-number range, and magnifications.
2. Establish a written data contract:
   - source folder;
   - ICC or original images;
   - channel mapping;
   - group-to-image-number mapping;
   - inclusion/exclusion boundaries;
   - magnification;
   - output names and destinations.
3. Ask for confirmation when any contract item is missing or materially changes previous work.
4. Apply deterministic organization and measurement only after the contract is stable.
5. Create a trace table before Prism or PowerPoint:
   - group;
   - simplified image name;
   - image number;
   - measurement;
   - source cell or selection marker.
6. Build Prism data from the trace table, not from memory or a prior deck.
7. Build each slide from the same trace table and exact image source folder.
8. Validate counts, IDs, channels, source paths, image proportions, and exclusions before delivery.

## Confirmation gates

Pause for explicit user confirmation before:

- deleting, moving, or bulk-renaming source images;
- interpreting an inclusive/exclusive image-number boundary;
- selecting a threshold or display range;
- deciding which channel is the measured fluorophore;
- switching between original, ICC, scale-bar, or re-exported images;
- treating colored spreadsheet cells as exclusions;
- excluding outliers or biological replicates;
- choosing statistical tests;
- generating a full slide deck when only a layout example exists.

For a deck, produce one representative sample slide first unless the user has already supplied an edited sample. Treat the latest edited sample as the layout authority, but continue using the current trace table for image IDs.

## Deterministic tasks

Proceed without additional confirmation when the rule is already explicit and no destructive action is involved:

- inventory and count files;
- detect missing channel triplets;
- simplify names without changing identifiers;
- separate magnifications when metadata or verified image evidence is available;
- generate ImageJ macros using the requested channel and statistic;
- reshape verified records into Prism Column or Grouped tables;
- rebuild lookup sheets from an already-confirmed exclusion rule;
- assemble slides from a confirmed trace table and source directory;
- render and check workbooks or presentations.

## Scientific boundaries

Do not decide biological expectations, threshold validity, normalization, outliers, or ANOVA design from appearance alone. Present evidence and alternatives, then ask the user to choose when the decision affects conclusions.

Prefer raw quantitative intensity over display-mapped RGB values. If measurement is performed on thresholded or display-ranged exports, state that the result reflects the mapped image and may contain clipping or zeros.

## Handoff

Report:

- exact source folder;
- exact output files;
- inclusion and exclusion rules;
- final group counts and image IDs;
- channel order;
- magnification;
- any unresolved scientific decisions;
- whether the output was visually verified.
