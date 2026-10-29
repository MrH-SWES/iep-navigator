# IEP Navigator - October 28 PDF mapping: workbook reconciliation

**Draft-only reference PDF:** `P20765!13!wasandbox!21-31-51-481435!10-28-26.pdf`  
**SHA-256:** `783317ded2ba1f896f56c57dfd525793668bc95384f415b486c81f703fc3110f`  
**Workbook now available:** `replacements_completed.xlsx` (118 rows, verified against field IDs and marker IDs in original source inventory).

## Three separate states - do not conflate

| Evidence layer | Result | Meaning |
| --- | --- | --- |
| Original IEP Online replacement run | 114 `VERIFIED` + 4 `VERIFIED_DEVIATION` | The reported editor values were saved and read back by re-entering screens. |
| This PDF, printable bracketed placeholders | 90 of 118 | Locations verified in the supplied 27-page PDF, by page/section/position. |
| No confirmed PDF occurrence | 28 of 118 | No defensible printed location in this export; **not** an editor-save failure. |
| PDF page 4, old markers | 6 tokens in three signature rows | **Output discrepancy:** bracketed values found elsewhere, but stale markers still print here. |

## Corrections reconciled

- `0011` `F0050`: `[Reason for participant excusal]` is the actual saved value and the workbook expected value. Previous navigator said `[Enter excusal reason (administrator/designee r]`; corrected in the app display.
- `0012` `F0053`: `[Method of prior agreement]` is the actual saved value and the workbook expected value. Previous navigator said `[Enter method of prearranged agreement (adminis]`; corrected in the app display.
- `0088`, `0090`, `0092`, `0093`: `[Present Levels of Performance]` was already used in the navigator mapping and matches the four `VERIFIED_DEVIATION` saved values.

## 6 mixed printed-output fields

On page 1, participant first/last-name placeholders appear in the expected row order and were position-matched. On page 4, the signature rows still have their exact old unique markers: `0007`, `0008`, `0013`, `0014`, `0015`, `0016`. The new CSV explicitly lists both coordinate sets. Cause of the discrepancy is unknown; a separate rendering path or snapshot mismatch is a possibility, not an established fact.

## Fields and non-text overlays

The existing app was **not rebuilt**. It retains its 416 field records, dashboard navigation, screenshots, 27-page PDF preview, 108 text hotspot fragments, and 350 existing non-text decision/checkbox region records. The latter 350 were **preserved but not reverified**; transition tables on pages 11-16 in particular require visual QA before relying on their positional click targets.

Field mapping uses a section- and page-scoped search of the attached PDF, with older known regions as anchors; repeated first/last participant placeholders on page 1 were differentiated by label, top-to-bottom row, and first/last column rather than matching first text occurrence. The two corrected 0011/0012 prompts still have no verified printed positions, so none were invented. `field_to_pdf_mapping_RECONCILED.csv` preserves positional rectangles and editor confirmation separately for all 118 fields.

## Still unresolved

- 28 saved text fields do not have a confirmed printed occurrence in this PDF.
- Six page-4 signature tokens do not reflect the saved editor values, despite the page-1 placeholders.
- Three previously mapped fields missing expected print in the fresh version: `F0157` (`0066`), `F0161` (`0071`), `F0167` (`0070`).
- Non-text overlay geometry was not individually revalidated after PDF reflow.
- Original separately authored `run_log.md` is not present; user provided narrative plus complete `replacements_completed.xlsx` workbook, both reflected in `RUN_LOG_RECONCILED.md`.

**No changes to IEP Online, Google Drive source, public GitHub repository, eligibility, placement, consent, school records, finalization, or transmissions.** The supplied PDF remains a sandbox draft.
