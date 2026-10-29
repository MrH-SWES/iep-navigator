# IEP Online 3.0 sandbox - language-only replacement run log (reconciled)

**Run date:** 2026-10-28  
**Record:** Sandbox School > Test Student20608 (IEP30TEST20608) > IDEA > Initial IEP  
**Original source supplied:** `replacements_completed.xlsx` (118 records) and the associated user-supplied replacement run-log narrative.  
**Verification scope:** saved values read back after leaving/re-entering relevant IEP Online sections/modals. This does **not** prove that every PDF template prints the same value.  
**Safety:** sandbox draft only; no eligibility, placement, services, decisions, signatures or finalization changed during the reported run. No app-side attempt to change the sandbox has been made in this reconciliation.

## Recorded results

| Outcome recorded by the original run | Rows |
| --- | ---: |
| VERIFIED | 114 |
| VERIFIED_DEVIATION | 4 |
| Not verified, skipped, conflicted, or rejected | 0 |
| Total | 118 |

The four run-time deviations are `ZZMAP0088ZZ`, `ZZMAP0090ZZ`, `ZZMAP0092ZZ`, and `ZZMAP0093ZZ`: actual saved text `[Present Levels of Performance]` instead of the truncated `[Present Levels of Performance (i.e]`.

**Two earlier CSV-normalization repairs:** `ZZMAP0011ZZ` and `ZZMAP0012ZZ` had already been fixed in the workbook's `updated_placeholder` column, but the older `IEP_Navigator_Placeholder_Changes.csv` and prior navigator display still showed malformed/truncated prompts. The actual workbook prompts are `[Reason for participant excusal]` and `[Method of prior agreement]`. The navigator display prompts are now corrected. These two were not counted among the four run-time deviations.

## Saved editor state versus PDF rendering

The attached October 28, 2026 PDF (SHA-256: 783317ded2ba1f896f56c57dfd525793668bc95384f415b486c81f703fc3110f, 27 pages) has six literal `ZZMAP` tokens still printed on its cover-page signature rows (page 4). The workbook states that each of those fields was later read back from the editor with new bracketed values. This difference is a **PDF-output discrepancy**; it does not establish that the editor save failed or why the PDF contains stale values.

Ninety of 118 text fields have one or more *confirmed visible printed placeholder locations* in this PDF. Twenty-eight were reportedly saved in the editor but have **no confirmed printable location in this particular export**; do not treat those as save failures. Six of the 90 also have the old printed marker on page 4, and so are tracked separately as mixed-output cases.

Page-4 residual fields: F0043 (`ZZMAP0007ZZ`), F0044 (`ZZMAP0008ZZ`), F0054 (`ZZMAP0013ZZ`), F0055 (`ZZMAP0014ZZ`), F0056 (`ZZMAP0015ZZ`), F0057 (`ZZMAP0016ZZ`). Check the signature/participant template linkage or print data snapshot before inferring a persistence problem. Never silently replace rendered text or alter source records.

## Original methodology reported

Each updated field was located by its original marker before entry, typed via IEP Online's input/CKEditor event handling, saved through the normal section or modal SAVE control, then verified by returning to the dashboard and reopening the relevant section. Full browser F5 reload was avoided because it broke the sandbox session. The final editor sweep found no markers. The replacement run did not produce this PDF or finalize the IEP.

## Retained files

- `replacements_completed.xlsx` - original 118-row workbook, unchanged.
- `replacements_completed_source_rows.csv` - unmodified tabular extraction from workbook.
- `IEP_Navigator_Placeholder_Changes.csv` - older mapping CSV, retained as provenance (has two stale truncated prompts).
- `field_to_pdf_mapping_RECONCILED.csv` - joined editor and PDF states, section/location coordinates, discrepancies, and navigation.
- `index.html` - same navigator with only two corrected display prompts.

The exact original separately-authored `run_log.md` file was not supplied. This note reconstructs the reported run in writing and does not purport to be that original file.
