# End-to-end workflow

## 1. Inventory and source control

- List LIF, TIFF, CSV, XLSX, IJM, PPTX, and metadata files.
- Record file counts, image-number ranges, channel suffixes, and folder structure.
- Keep original acquisitions read-only.
- Create processed outputs in clearly named folders.
- Record the exact image source used for every downstream artifact.

Typical Leica channel triplets:

- `*_ch00_SV.tif`: brightfield or first exported channel;
- `*_ch01_SV.tif`: red fluorescence when verified by the experiment;
- `*_overlay.tif`: merged image;
- `*_ICC_*`: ICC-processed counterpart.

Do not assume suffix meaning without checking one representative field or user documentation.

## 2. Group and magnification organization

- Parse image numbers without discarding original identifiers.
- Apply group prefixes only after confirming exact boundaries.
- Treat wording such as “before 51,” “from 52,” or “108 is not retained” as boundary-sensitive.
- Verify magnification from metadata when possible. If metadata is unavailable, use field-of-view/cell-size evidence and ask the user to confirm ambiguous cases.
- Move files only after presenting the proposed list or when the user has explicitly authorized the rule.

## 3. Fluorescence export and thresholding

- Separate acquisition settings from display settings.
- Compare groups only when exposure, gain, channel, and export mapping are consistent.
- Use normal/control fields to check background, but do not force them to zero solely to improve contrast.
- Discuss threshold/display-range selection with the user because it changes the visual and sometimes the measured values.
- Prefer measurements from raw or consistently processed single-channel images.

## 4. ImageJ batch measurement

For mean red-channel intensity:

1. Open one image.
2. Split channels.
3. Select the verified red channel.
4. Run `Measure` for mean intensity only.
5. Preserve the simplified image name beside the measurement.
6. Repeat for all matching TIFFs.
7. Save CSV to an ASCII-safe path when an older ImageJ build cannot handle Chinese paths.

Avoid background subtraction, rolling ball, thresholding, or automatic segmentation unless the user requests and validates those steps.

Validation:

- processed file count equals expected red-channel image count;
- image names remain traceable;
- results do not accidentally include brightfield, overlay, or non-ICC files;
- zeros are checked against the actual red image.

## 5. Spreadsheet and Prism preparation

Maintain three logical layers:

1. raw/complete data;
2. selection trace table;
3. Prism-ready table.

Recommended trace columns:

- `Group`
- `Image_Name`
- `Image_No`
- `Mean`
- `Source_Cell`
- `Included`
- `Exclusion_Reason`

If the user uses yellow fill as an exclusion marker:

- confirm yellow means exclude;
- read the exact named sheet;
- match each numeric cell back to the complete dataset by group order and image number;
- create/update a lookup sheet and a Prism sheet;
- report retained counts and IDs.

Prism formats:

- Column: one group per column, replicates down rows;
- Grouped: use when two experimental factors need explicit row/column structure.

## 6. Statistical discussion

Ask about:

- independent or paired observations;
- biological or technical replicates;
- experimental factors;
- normality and variance assumptions;
- planned comparisons;
- whether magnifications or acquisition batches are pooled.

Do not select one-way/two-way/repeated-measures ANOVA solely from column appearance.

## 7. PowerPoint image panels

- Use the current trace table as the only image-ID authority.
- Use the exact confirmed folder as the image-source authority.
- For each selected field, match the brightfield, fluorescence, and overlay triplet.
- Keep image proportions; never stretch microscopy images.
- Preserve scale bars when required.
- Create one slide per group and keep channel order consistent.
- When the user provides an edited sample, copy its layout and typography but replace IDs from the current trace table.

Quality checks:

- page count equals group count;
- each page has the expected number of fields and channel images;
- no channel triplet is missing;
- titles and group order match the spreadsheet;
- no stale images remain from an earlier threshold export;
- scale bars are visible and not cropped;
- render every slide before delivery.

## 8. Final audit

Provide a compact audit record:

- source workbook and sheet;
- source image folder;
- threshold/export label;
- magnification;
- selected image IDs by group;
- total measurements and slide images;
- outputs and verification status.
