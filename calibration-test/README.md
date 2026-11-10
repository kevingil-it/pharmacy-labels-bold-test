# Label Center — Calibration Test 1.0

This directory contains isolated copies of Motivated 2.4.4 and Cottonball 2.4.5 from production commit `58f92f108c04f88cb7afe4a3a7c76bc56ca61bfa` (November 10, 2026).

Open `index.html` to select a clinic and follow the test procedure. The files work together in this folder, either on GitHub Pages or extracted locally. Keep the official entry page and programs in their current locations.

## Purpose

Establish whether the reported centering difference is constant, varies between labels, or affects only the start of a job. This is an isolated baseline, not an automatic printer calibration system or a verified alignment fix. The browser does not observe the printed sticker or its edges.

## Changes in this copy

- A screen-only test banner and shortcuts to the existing alignment controls.
- Separate browser storage for test printer settings and medication catalogs.
- Distinct page titles and exported printer-profile filenames.
- A separate landing page with a controlled one-label / ten-label test procedure.

The print engine, page dimensions, medication geometry, QR generation, embedded fonts, date validation, fit checks and original print actions are preserved. The test banner is hidden by the existing print stylesheet. No production links are redirected to these files.

## Storage boundaries

Both test apps use `label-center-calibration-test-printer-v1`. Motivated uses `label-center-calibration-test-compound-labels-catalog-v1`; Cottonball uses `label-center-calibration-test-cottonball-labels-catalog-v1`.

They do not read or write the production printer or catalog keys. They share one test printer profile with each other on the same browser and origin. Initial X / Y are zero unless a test profile was previously saved. A profile can be imported explicitly; imported values are saved only when the user chooses Save printer settings. The bundled corrected catalog is present, but custom production catalog entries are not copied automatically.

Windows driver settings and hardware settings remain shared. Changing those externally can also affect production. For the first run, record and retain the working driver values. A zero-driver experiment requires a separate test setup or recording and restoring the existing values.

## Test procedure

1. Record the PC, printer, physical label diameter, gap, driver page size, driver Top / Left, and test X / Y. Keep stock and print path constant.
2. Select the matching printer resolution and physical diameter. Current 1-inch stock uses a 1.00-inch page and a 0.95-inch content area.
3. Set test X / Y to zero. Print one alignment target through Chrome at 100% scale, with matching paper size, no margins, headers / footers off, and one Chrome copy.
4. Print ten targets. Retain the whole numbered strip. Compare the first, middle and final labels.
5. For a consistent small offset, adjust using the existing one-dot controls, reprint, then save the test profile. Positive X moves right; positive Y moves down. At the nominal 300-dpi Zebra setting, one native dot is 1/12 mm, approximately 0.083 mm.
6. If position varies, record the pattern rather than compensating each label manually. Check stock, guides, paper size and media calibration as a separate investigation. Do not change several settings at once.
7. After targets are consistent, compare short and long names, Compound / Fill for Motivated, and Cottonball VX.5. Repeat targets after a roll change. Verify a physical QR scan before any operational use.

The existing fit checks may reject large software shifts. Do not weaken them to hide a page-size, driver or feed-position problem.

## Verification

`Source-Verification.json` records the official and test SHA-256 hashes and scoped replacements. The build reverses every test-only edit and asserts byte-for-byte equality with the original official HTML. `Test-Verification.json` records storage isolation and shortcut / calibration-output checks. `SHA256SUMS.txt` covers the package files.

No physical printer or scanner has been tested by this software verification. An on-screen target cannot establish physical alignment or feed repeatability.
