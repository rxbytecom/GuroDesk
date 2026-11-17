# Form templates and policy sources

Source workbooks retrieved 17 September 2026; application layout checks completed for release 1.3.0. The app works offline with 22 selectable layouts. These are reproductions based on published workbooks, not LIS-issued documents or a claim of DepEd certification. School review is required before submission.

## Sources and choices

| Reports | Choices | Published source |
| --- | --- | --- |
| SF1, SF2 | Kindergarten–Grade 10; separate SHS variants | [SDO Catanduanes school forms](https://catanduanes.deped.gov.ph/new-school-forms.html), [LIS support](https://support.lis.deped.gov.ph/support/) |
| SF5 | Kindergarten SF5-K; Grades 1–10 DO 8, s. 2015; SF5A-SHS; Grade 12 SF5B-SHS | [LIS support downloads](https://support.lis.deped.gov.ph/support/) |
| SF9 | Kindergarten; Grade 1 with five PACE attachment pages; Grade 2; Grade 3; Grades 4–10; Grades 11 and 12 Academic/TechPro; SSHS semestral | [DepEd Learning System guide, School Forms link](https://sites.google.com/deped.gov.ph/lsguide/budgets-of-work), [SF9 source folder](https://drive.google.com/drive/folders/1N4rh9vXbR4Z4YaW2Od5LJYtFTIMkwdPB) |
| SF10 | ES and JHS March 2025 front/back; legacy SHS front/back/annex; corrected strengthened SHS 2026 front/back/annex | [LIS support downloads](https://support.lis.deped.gov.ph/support/) |

SF9 choices are labeled **SY 2026–2027**. Schools must select the version applicable to their year and curriculum. Selecting a template does not change the school's grading policy or convert quarterly marks into terms. Specialized programs and division-specific modifications may need a different prescribed workbook. Kindergarten uses SF9/SF5-K; an elementary SF10 is not substituted for Kindergarten.

Unmodified downloaded workbooks are in `assets/forms/*.xlsx`. URL/Drive-ID inventories are `sources.json` and `sf9-sources.json` in that directory. The Kindergarten SF9 Drive ID is `1Oyyrl4G3kUQ-j4-vjuUaLp-W3Ba04_JD`. The app's **Save original Excel template** button saves the relevant original file for manual completion, without internet. Original files may contain sample entries, formulas, input sheets, and instructions; they are not populated with the user's school records.

## Layout implementation

`shared/form-templates.ts` defines grade compatibility, source worksheet ranges, orientation, and paper size. `npm run forms:compile` reads source workbook cells, merges, borders, fonts, dimensions, and embedded images into `assets/forms/layouts.json`. Runtime reports use this compiled layout without executing spreadsheet formulas. Cached formula values and sample identities are not treated as school data.

Print output uses A4, Legal (8.5 × 14 inches), or Folio (8.5 × 13 inches), with fixed 6 mm margins. Class lists continue across pages; different classes and individual learner records remain separate. Some inconsistent source-row merges are normalized for readable populated rows. Excel and browser typography/pagination can differ; use the original workbook when exact Excel output is required.

## What is populated and what needs completion

- School identity, learner identity, LRN, available address/guardian fields, and class information populate where supported. Missing parent/religion/IP fields remain blank.
- SF2 uses actual school-calendar days and recorded attendance. Blank in a populated day column means present; `x` means absent and `◩` means late. `?` means attendance has not been recorded and must be resolved before submission. Unrecorded days are never silently marked present. Monthly statistical summaries and dropout-reason sections require review/completion.
- SF5 Grades 1–10 uses approved final subject averages and saved promotion status. Kindergarten ECCD/appraisal, SHS semester completion, graduation eligibility, national certification, and aggregate summary boxes are not inferred from generic grades.
- Numeric SF9 term marks populate only from a three-period policy and matching learning-area names. Unmatched subjects, semestral results, general-average/remark boxes, values, narrative comments, competency ratings, and promotion/certification details require teacher completion. Kindergarten and Grade 1 include descriptive/competency layouts without converting numeric grades into observations.
- SF10 ES/JHS maps available historical final subject records within the template's grade band. Historical quarterly ratings, eligibility, remediation, transfer certifications, and SHS semester/track records require verified source records and manual completion.
- Signatures, dates, and details not captured by the app must be completed and checked by the school. A checked review box does not provide or certify missing information.

Older saved `review-1` reports retain their original internal-review format. New reports generated through the grade/template choices store their selected template ID. Learner Profile remains an application report, not a prescribed DepEd school form.

## Validation

Automated tests cover all 22 layouts, grade compatibility, escaping, all-grade SF9 choices, Grade 1 attachments, incompatible grading-period handling, and 100-learner continuation cases for SF1/SF5 variants. Hidden Electron rendering checks inspect populated fictional forms for clipped text and generate preview images and PDFs. Packaged desktop checks exercise generation and offline original-workbook export. These checks do not replace school acceptance or a physical printer test.

The configurable grading/transmutation/promotion rules still need school approval. Layout selection alone does not implement every curriculum-specific assessment policy.

### Published presentation update (1.6.1)

The renderer measures glyph widths, fits text within source geometry, preserves Excel overflow into blank cells, and draws merged-cell perimeter borders above cell backgrounds. Original workbook files and page dimensions are unchanged. Regenerate saved HTML report snapshots to use the updated presentation. This is a presentation correction, not certification of official forms.

### Compact generated reports (1.6.2)

At user request, generated published reports omit unfilled learner slots and unused attendance-day columns while retaining required fields, summary panels and signature sections. Continuations repeat school identity and share a print scale. This compacts the generated presentation; the original downloadable workbooks remain unchanged. Saved reports must be regenerated.

### Restored report grids (1.6.3)

The 1.6.2 compaction changes were reverted at user request. Generated reports again retain the original rows, columns and page ranges from 1.6.1. Only a shared print scale remains to align continuation pages. Regenerate saved reports after updating.


### Report-card data coverage (1.6.4)

Attendance uses saved records for the selected enrollment and school year. Published present counts include late entries; absent counts include excused and unexcused absences, consistent with the existing published-card convention. Unrecorded days remain unknown rather than suppressing known monthly counts. Future empty months do not suppress recorded totals. Early-grade September is displayed once because term date boundaries are not stored. Preview notices explain this limitation, unmatched subjects, incompatible grading periods and fields requiring teacher verification. No term conversions or new grading calculations are introduced.


### Published grade coverage (1.7.1)

Generated SF9/SF10 output includes a clearly identified supporting grade record when numeric period grades cannot be represented by the selected source form. The original workbook grids, fields and scales remain unchanged. This page is an application-generated supporting record, not a new official DepEd template or a substitute for descriptive, semester-specific or verified historical assessments. Approved grades, including zero, are shown by actual configured period; missing grades remain unavailable. No conversion between quarters, terms, semesters or descriptive ratings is inferred.

### Main card period mapping and age (1.7.2)

Numeric SF9 main columns now display saved approved grades through an explicit period-to-column mapping, defaulting to the first three periods. The mapping is visible in report configuration and preview notices, and retained in generated-report filters; four-period supporting pages identify it alongside all period grades. Original grid labels and dimensions are retained. No term/semester equivalence or conversion is inferred. Age is completed years as of the user-visible reference date, defaulting to today; missing or invalid birthdates are not guessed.
