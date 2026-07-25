# Decision boundaries

## Proceed automatically

These tasks are normally deterministic after the user has supplied a complete rule:

- inspect files and folders;
- count images and channels;
- identify missing triplets;
- simplify filenames while preserving IDs;
- build a non-destructive rename/move plan;
- run a confirmed ImageJ measurement recipe;
- convert a confirmed selection into Prism format;
- update a lookup sheet from confirmed markers;
- build slides from a confirmed lookup table and image folder;
- render and validate outputs.

## Require explicit user confirmation

Ask before actions that change data, scope, or traceability:

- deleting images;
- moving or renaming source files;
- interpreting inclusive/exclusive number boundaries;
- overwriting an existing workbook or deck;
- choosing which of several folders is authoritative;
- switching between ICC and non-ICC images;
- switching threshold/export versions;
- interpreting fill colors or annotations as exclusions;
- accepting a slide layout before batch generation.

Use a short confirmation that includes exact targets and boundary examples.

## Require discussion, not a yes/no shortcut

These choices affect scientific conclusions and should be discussed with evidence:

- fluorescence threshold or display range;
- raw intensity versus display-mapped RGB measurement;
- expected direction between oxygen conditions;
- outlier removal;
- normalization by cell number, area, or background;
- combining 10× and 20× data;
- pooling acquisition batches;
- one-way versus two-way ANOVA;
- independent versus paired or repeated-measures analysis;
- biological versus technical replicate treatment.

## Never infer silently

- channel identity;
- oxygen-group boundary;
- whether an endpoint image number is included;
- microscope magnification;
- scale-bar calibration;
- whether yellow means exclude;
- which worksheet is authoritative;
- whether a user-edited sample changes only layout or also image selection;
- whether a new export supersedes earlier measurements.

## Recovery rule

When conflicting instructions or artifacts appear:

1. stop mutation;
2. inventory the conflicting sources;
3. identify the latest user-edited authority for each category:
   - layout;
   - image IDs;
   - image source;
   - quantitative values;
4. state the proposed authority map;
5. resume only after confirmation if the conflict changes results.
