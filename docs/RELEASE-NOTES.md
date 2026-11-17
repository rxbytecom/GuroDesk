# Release 1.9.0 - Free for all teachers

- **GuroDesk is now free.** The three-day trial, license codes, activation files and the activation screen were removed. Every feature works on every computer, with no payment or internet connection.
- **Developer credit.** The login screen, the bottom of every page, the installer and the user guide show "Developed by Raymart Hernandez".
- Older installations upgrade normally; school records are kept and any saved activation is simply ignored.

# Teacher records, sharing and new school forms

- **Import learners from Excel / LIS.** Reads the LIS (SF1 / masterlist) export, the app's own export or any class list: the header row and columns (LRN, one-column or separate names, sex, birthdate in any common format, address, parents or guardian, contact) are found automatically. A preview shows new learners, learners already saved and rows with problems; the learners can be enrolled in a class in the same step.
- **Share grades between computers.** Subject teachers save a grades file (Grades › Share grades); the adviser opens it, sees what will be added or changed, and imports it. Learners are matched by LRN and classes by grade level and section; missing subjects are added. Teacher Mode publishes imported grades; Multi-User Mode submits them for approval. A class record with its own activity scores is never overwritten.
- **Learner Records page** for what the forms need besides grades and attendance:
  - Report card comments per term. Grades 2–12 print in the card's Teacher's Comments / Remarks boxes; Grade 1 prints "What your child can do" and "learning to improve"; Kindergarten prints on the lined comment boxes. (The 2026 SF9 no longer has an Observed Values section; it has these comment boxes.)
  - Kindergarten checklist ratings (BG/DV/CO) and Grade 1 PACE ratings (A–E), entered one competency at a time for the whole class, printed in the official rating boxes, including the colored macro-skill squares.
  - Height and weight with automatic BMI, nutritional status and height-for-age (WHO 2007 growth reference, 5–19 years) for SF8.
  - Class book list with date issued, date returned and remarks for SF3.
  - Learners needing help: flagged automatically for a grade below passing or absences of 20% or more, with a record of interventions and results.
- **New forms:** SF3 (books), SF4 (monthly learner movement and attendance), SF6 (promotion and proficiency summary), SF8 (health and nutrition), the honor roll, a progress notice for parents, and the learners-needing-help list. GuroDesk lays these out with the DepEd columns; no DepEd workbook is bundled for them.
- **Honors:** Grades › Honors ranks learners by general average (not rounded) with cut-offs set in Settings (default 90 / 95 / 98, optional lowest final grade).
- **Class record to Excel:** E-Class Record › Save as Excel writes the term's class record in the e-class record arrangement (scores, totals, PS, WS, initial and term grade, males then females).
- Kindergarten and Grade 1 cards fill the child's age in years and months (start of the school year, and end of the school year for Grade 1). The Kindergarten card now prints the teacher's name and LRN in the correct boxes.
- Dashboard reminder when learners need help. Older backups restore into this version (the new table is added during restore).

# Unreleased - automatic DepEd grading (DO 015, s. 2026)

- The app is now called **GuroDesk** (window title, sidebar, sign-in and license screens, installer, Start-menu and desktop shortcuts, owner License Manager and documentation). Existing school data, backups and activation keys carry over: the data folder stays at `%APPDATA%\deped-smart-school`, and installing GuroDesk over DepEd Smart School upgrades it in place.
- One-click **Use DepEd DO 015, s. 2026** preset in Settings: three terms, passing grade 75 and the adjusted transmutation table. The table is shown as readable rows; JSON editing moved under "advanced". New installations start with these values (approval still required).
- Examinations follow DO 015: Summative Test 1 (30%), Summative Test 2 (30%) and Term Examination (40%). Existing "combined" examination activities keep working.
- Subject weights fill in automatically from the learning area (blank weight fields = DepEd weights). **Apply DepEd weights to all subjects** updates the catalog in one step.
- Saved activity-score grades are recalculated automatically when subject weights or the grading policy change, including when the policy is approved. **Publish saved grades** is no longer needed after approval.
- Teacher Mode can adjust subject weights and the grading policy after grades are saved (changes are audited and recalculated). Multi-User Mode keeps the return/unlock requirement.
- Grading periods are named "Term" for three-period years and "Quarter" for four; unused period rows are hidden.
- Activity titles are optional and numbered automatically per category.
- Removed the "Readable report · larger text" option from DepEd Forms and Report Cards; reports always use the official DepEd form layout.
- Redesigned Attendance for easier use: larger text, one large labelled button per status (Present, Absent, Late, Excused), Previous / Next / Today day buttons that skip weekends, the full date in words, live counts, "Mark the rest present" (keeps statuses already chosen), a Save bar that stays on screen, a warning before leaving unsaved attendance, and weekend / no-class-day warnings. Notes open only when needed. Past records show the selected month, newest first.
- Redesigned E-Class Record as numbered steps with larger text: class/subject and term tiles, activities grouped by Written or Oral Works / Performance Tasks / Examinations with their weights and one Add button per type (no category list to pick from), progress on each activity ("10 of 12 scored"), large score boxes, a Save bar that stays on screen, a warning before leaving unsaved work, and a plain "what to do next" for every learner's term grade. Direct-grade entry uses the same layout.
- Redesigned Grades & promotion: one card per class, subject and term (instead of one row per learner) with Approve / Send back / Unlock buttons and filters such as "Waiting for approval"; a Promotion tab with class tiles and "Calculate decisions for the whole class".
- Attendance, E-Class Record and Grades & promotion now use the app's normal text size (the Text size control enlarges them) and its standard header, tabs, panels and tables. E-Class Record shows activities beside the score sheet; Grades & promotion lists one row per class, subject and term.
- Redesigned Student Profiling (search and class filter, labelled View / Edit / Archive buttons, learner form grouped into Learner, Parent / guardian, Address and School history), Enrollment (status counts, a "Learners not yet enrolled" list to tick and enroll into a class in one step), Classes & sections (one row per class with its subjects, "Add subjects to this class" to add several at once) and DepEd Forms / Report Cards (numbered steps, labelled form choices, tick-box learner selection instead of Ctrl-click, rarely used settings under "More options", Preview / Save as PDF / Print).
- Dashboard is now a simple daily home: today's attendance status for each class with a Take attendance button, automatic reminders (grades waiting for approval, missing scores, learners not enrolled, classes without subjects, unapproved policy, overdue backup) each with one button, shortcuts, four key numbers and two charts. School reports has labelled filters and clearer charts.
- Labels use DO 015 terms: Written or Oral Works, Product or Performance Tasks, Examinations.

# Unreleased - official DepEd SF9 format

- Numeric SF9 cards (Grades 2–12) print the official performance descriptors again: 90-100 Advancing, 80-89 Benchmarking, 75-79 Connecting (Passed); 65-74 Developing, 0-64 Emerging (Failed). This reverses the 1.8.3 legend override. The readable layout uses the same descriptors.
- Signature captions keep the official "School Head" label (reverses 1.8.4). The Settings Principal name still signs the card.
- Official learning-area rows keep their printed names. Subjects no longer replace another learning area (e.g. Science in the Grade 2 Makabansa row); unmatched subjects go to the supporting page. Only SHS elective placeholder rows take the subject name. Use Report row to link differently named subjects.
- Remarks print Passed (75 and above) or Failed, matching the form's formula, for each learning area and the General Average.
- Grade 11 Academic elective terms shaded on the form stay blank; the elective's final grade is its open-term grade.
- Report Cards opens on the published form by default. Descriptor words on the Grade 1 card no longer break mid-word.
- Regenerate previously saved report cards after updating.

# Release 1.8.7 - Offline fixed-term licensing

- Adds signed, device-bound 1-month, 3-month and 12-month activation with visible expiry and clock rollback checks. Existing lifetime licenses remain valid.
- Owner Manager supports all inventories and displays duration and expiry. Reissuing a code preserves its original expiry.
- Expiry retains school records. Install over the existing app; do not uninstall to update.

# Release 1.8.6 - SF10 subject and learner synchronization

- SF10 scholastic sections use current class subjects or saved historical permanent-record subjects. Remedial tables no longer consume regular school-year records.
- Corrected learner name extensions and cleared source sample identity values. Each school-year block receives its own available metadata.
- Senior-high annexes show matching saved subjects and place other subjects in the existing Other Subjects rows, continuing on additional annex pages as needed. Unknown track, semester and passing results remain blank.
- Regenerate previously published reports after updating. Existing database records are unchanged.

# Release 1.8.5 - SF10 logo proportions

- SF10 ES, JHS, SHS and SSHS images preserve their original aspect ratio and stay centered in their source header boxes. Logos are no longer stretched to the worksheet anchor dimensions.
- Original workbook images, form fields, grid geometry, margins and page layout are preserved. Regenerate old reports after updating.

# Release 1.8.4 - Principal on report cards

- Report cards use Settings ? Principal for the default signatory again. Explicit report signatories still take priority.
- Published SF9 School Head labels now read Principal; readable report signature captions use Principal.
- Regenerate reports after installing over the existing app.

# Release 1.8.3 - report-card performance descriptors

- Numeric SF9 cards use the requested five-row legend: Outstanding (90?100), Very Satisfactory (85?89), Satisfactory (80?84), Fairly Satisfactory (75?79), and Did Not Meet Expectations (Below 75). The first four show Passed; the last shows Failed.
- Applied to readable and published layouts, with columns Descriptors, Grading Scale and Remarks. Grading calculations, approval rules and saved grades are unchanged. Kindergarten and Grade 1 competency scales remain separate.
- Regenerate previously saved reports after updating.

# Release 1.8.2 - report card school head and SF9-only screen

- Report card signatories now use the saved School head field before falling back to Principal. An explicit report signatory takes priority. Automatic previews refresh when the saved school signatory changes.
- Report Cards now offers SF9 only; other report types remain in DepEd Forms. Switching between these screens resets their report state.
- Regenerate previous reports after installing over the existing app.

# Release 1.8.1 - grouped record actions

- Moved Delete beside Edit, Report row or Review in the existing Actions columns for Subjects, Classes & sections, assignments, Enrollment and Grades. Student Profiling already grouped its actions. Deletion rules and confirmations are unchanged.

# Release 1.8.0 - delete actions for school records

- Added confirmed Delete buttons to Subjects, Student Profiling, Enrollment, Classes & Sections (including assignments), E-Class Record activities/direct grades, and Grades. Cancel leaves data untouched; server validation failures remain visible in the dialog.
- Unused parent records may be deleted. Linked enrollments, subjects and classes are protected. Student deletion includes guardians and documents only when no enrollment exists.
- Activity deletion includes its scores; Teacher Mode recalculates affected grades, while Multi-User draft grades are cleared for recalculation. Individual grade deletion retains scores and records approval history in the audit log.
- Existing role/class permissions, closed-year protection and Multi-User grade locks apply. Promotion decisions and permanent records block academic deletion. Saved/exported report copies are unchanged; regenerate reports after deleting records.
- Install over the existing app without uninstalling.

# Release 1.7.4 - automatic class subject lists

- Published numeric SF9 cards now automatically place all assigned class subjects in available learning-area rows, preserving familiar positions where possible and filling remaining rows with custom subjects. Unused template subject names are cleared without removing grid lines or columns.
- Manual Report row mapping is optional. Every grade remains attached to its assignment ID. Excess subjects are listed on the supporting pages, including names whose grades are not approved yet (grade cells stay blank).
- Semester cards also display assigned subject names; numeric period grades remain separate from semester results. Competency forms and permanent history retain their distinct source-data rules.
- Regenerate reports after installing over the existing app.

# Release 1.7.3 - subject names and published report rows

- Subjects can be filtered by assigned class. Readable report cards continue to show that class?s assigned subjects.
- New Report row action connects a subject to a numeric SF9 template row without changing its grades, weights or approval status. Matched published rows use the saved subject name.
- Conflicting mappings remain blank with a warning and supporting grades page; no arbitrary subject is chosen. Class-specific warnings now also appear in four-period years.
- Original grids, descriptive forms, semester fields and verified historical SF10 records are preserved. Install over the existing app and regenerate previously saved reports.

# Release 1.7.2 - main report-card grades and learner age

- Removed the blanket three-period restriction on the numeric SF9 main grade table. T1/T2/T3 copy approved grades from selected saved periods, defaulting to the first three. Report controls and preview notices expose this mapping.
- All configured periods remain on the supporting page when the form cannot hold them. Final Grade and General Average still require complete data under the existing policy; no conversion or averaging between selected columns is introduced.
- Published numeric SF9 Age now comes from the learner birthdate and the visible Age as of date (today by default). Invalid/missing/future-relative birthdates stay blank with a notice. The reference date is stored with the generated report.
- Added validation for duplicate or wrong-year period mappings and regression checks for the Grade 7 main Mathematics and Age fields. Descriptive and semester-specific fields still require appropriate source records.
- Install over the existing app without uninstalling; reopen Report cards or regenerate old reports.

# Release 1.7.1 - grades in every published card selection

- Published SF9 and SF10 now include a clearly labeled Saved subject grades supporting page when the original form cannot represent all saved approved period grades.
- Covers four-period years using three-term forms, unmatched subject names, descriptive early-grade forms, semestral SHS cards and current-year grades alongside permanent records. The original form cells and grids remain intact; no quarter-to-term/semester or numeric-to-descriptive conversion is invented.
- Compatible subjects and periods still populate the original cells. Added unambiguous Math/Maths matching to Mathematics. Unapproved grades are excluded with a preview notice.
- Supporting pages repeat learner identity, show all configured periods, and continue long subject lists without losing grades.
- Open Report cards for a fresh preview or regenerate previously saved reports. Install over the existing app without uninstalling.

# Release 1.7.0 - subject grade entry and automatic report cards

- Added a per-subject choice of direct grading-period grades or calculated activity scores, with access to subject settings from E-Class Record. Existing subjects keep their calculated method and weights.
- Teacher Mode saves publish each complete grade automatically when the grading policy is approved; corrections and incomplete grades update the saved grade record with audit history.
- Multi-User Mode retains draft, submission, approval, assignment restrictions and grade locks.
- Report cards load a fresh preview automatically. Existing exported files are unchanged.
- Entry methods are protected once assessments or grades exist; assignments with direct grades cannot be reassigned. No database migration or record deletion is required.
- Grading formulas and report layouts remain unchanged. Install over the existing app without uninstalling.

# Release 1.6.6 - simpler teacher score entry

- Added a four-step guide, full category names, larger score fields, entry counts and a simple saved-grade preview. Detailed calculations remain expandable.
- Enter/Shift+Enter moves between learners; invalid scores are highlighted and cannot be saved. Save/discard controls prevent switching activities with unsaved edits.
- Submission is available when saved grades are complete and policy approval is in place. Added an entry shortcut from Grades.
- Existing grading formulas, permissions, approval workflow, records and report layouts are unchanged. See GRADE-ENTRY.md.
- Install over the existing app without uninstalling.

# Release 1.6.5 - visible daily attendance

- Published SF2 now displays P = Present, A = Absent, L = Late, E = Excused, U = Unexcused, and ? = Unrecorded, with a matching printed legend. Unused dates and learner slots remain blank.
- Corrected SHS learner row mappings so attendance stays in learner rows and does not overwrite totals or guidelines.
- Original report rows, columns, continuation alignment, attendance records and calculations are preserved. Downloadable source workbooks are unchanged.
- Regenerate saved reports after updating. Install over the existing app without uninstalling.

# Release 1.6.4 - report-card data mappings

- Fixed published Kindergarten/Grade 1 attendance and the semestral SHS attendance/identity cell mappings.
- Monthly attendance now shows recorded counts even when other days are unrecorded; totals no longer disappear because future months are empty. Late counts as present; excused and unexcused absences count as absent in published cards. No attendance is invented for unrecorded days.
- September appears twice in the early-grade templates: monthly counts appear once, with a preview notice that term allocation requires verification.
- Added adviser/principal fallbacks, unambiguous subject-name matching and the existing computed general average. Only approved grades populate cards.
- Preview notices explain incompatible term configurations, unsupported semester/descriptive/transfer fields and unmatched subjects. Original report grids and calculations are unchanged.
- Regenerate saved reports after updating. Install over the existing app without uninstalling.

# Release 1.6.3 - restore original report grids

- Restored the original rows, columns, blank slots, attendance grids and page ranges from version 1.6.1.
- Kept only a shared print scale to align continuation-page columns with page one.
- Restored the original readable and internal-review layouts. Regenerate saved reports after updating.

# Release 1.6.2 - compact reports and aligned continuation pages

- Published class reports print only populated learner rows. Extra attendance-day columns are removed; remaining day columns share the available grid width.
- Required identity, subject, totals, remarks, summary and signature fields remain available. Original downloadable workbooks are unchanged.
- Continuation pages repeat school headers and use a common print scale; promotion summaries flow independently from compact learner tables. Empty continuation pages are omitted.
- Readable reports no longer add placeholder data rows or blank assessment-entry rows.
- Regenerate saved reports after installing this update. Install over the existing app without uninstalling.

# Release 1.6.1 - published report presentation

- Improved published SF1, SF2, SF5, SF9 and SF10 typography using measured font widths and available cell space.
- Restored merged-cell perimeter borders and consistent print line weights; improved label/value alignment and signature readability.
- Large reports now load from isolated local preview files instead of size-limited data URLs, preventing preview and PDF export failures. Preview files are removed when their windows close.
- Preserved original workbook files, template page sizes, sections and required content. Dense registers still use smaller text where the prescribed structure requires it.
- Select Published form layout and regenerate saved reports to apply these changes. Install over the existing application; do not uninstall to update.

# Release 1.6.0 — optional Single-User Teacher Mode

- Added Application Mode selection in Settings and first setup. Existing installations default to Multi-User / Admin Mode.
- Teacher Mode opens directly to Dashboard, uses a local teacher profile, and creates no user account or password.
- Hidden account management and authentication controls in Teacher Mode; school workflows, grade review, reports, printing, PDF, and backups remain available.
- Preserved existing users, permissions, learner records, assignments, calculations, and report layouts. Account-free subject assignments are supported through a data-preserving migration.
- Backups retain the mode/profile; older compatible backups are migrated before restore.
- See [Teacher Mode instructions](TEACHER-MODE.md). Install over the existing app without uninstalling.

# Release 1.5.0 — readable report layouts

- New default Readable report layout for SF1, SF2, SF5, SF9, SF10, and learner profiles. Uses A4, 10–11 pt body text, complete table borders, aligned identity fields, and signature lines.
- Attendance and wide registers are divided into smaller sections to keep text readable. Remarks and acknowledgment sections have writing lines.
- Published workbook layouts and original Excel templates remain available as a separate choice. Readable reports are not prescribed DepEd forms.
- Regenerate existing saved reports to apply the new formatting; saved report snapshots keep their original layout.
- Install the update over the existing app. Do not uninstall to update, because uninstalling removes local school data.

# Release 1.4.0 — adjustable reading size

- Added a Text size toolbar available before sign-in and throughout the application, including activation screens.
- Choose 100%, 125%, 150%, 175%, or 200%, use A− / A+, or Reset to standard size. The preference is saved locally on the current Windows profile and restored after restart.
- Application labels, inputs, buttons, menus, tables, and headings scale together. Larger sizes wrap navigation and stack forms to keep controls accessible.
- Printed forms and generated PDF typography retain their template sizes. No database migration or license reactivation is required.

# Release 1.3.0 — grade-specific report templates

- Added Kindergarten–Grade 12 selectors and 22 published-workbook-based choices for SF1, SF2, SF5, SF9, and SF10, including SHS variants and Grade 1 PACE attachments.
- Preserved source headings, table structure, logos, front/back/annex sections, and template-specific paper orientation. Class lists continue across pages without dropping learners.
- Added offline export of the original Excel workbook for manual completion of fields not stored in the app.
- PDF/native print uses the chosen form's A4, Legal, or Folio size. Existing saved review reports remain accessible.
- No database schema change or license reactivation is required for an upgrade. See [template sources and completion limits](POLICY-SOURCES.md).

# Release 1.2.0 — easier offline activation

- Two-step activation panel: save a request and open the seller's activation file.
- Copy Device ID, optional pasted-key entry, clear purchase-code guidance, and a lifetime activation success screen.
- Separate owner License Manager, launched by double-click, imports requests and issues customer activation files without PowerShell.
- Existing codes and signed activation keys remain valid. No license inventory is regenerated.

# Release 1.1.1 — remove saved data on uninstall

- Windows uninstall now deletes the current user's app-data directory, including records, attachments, automatic backups, caches, and trial/activation state.
- Normal upgrades retain data. Manual exports outside the app-data folder and the owner's private license inventory remain untouched.
- Reinstalling after uninstall starts a fresh trial; an existing device-bound activation key can be reapplied on its original device.

# Release 1.1.0 — trial and offline lifetime activation

- Added a 72-hour trial, remaining-time indicator, and manual offline activation panel.
- Added signed lifetime licenses bound to the Windows device identity, enforced in the main process.
- Generated 50 unassigned lifetime entitlements in a private owner inventory. The owner tool permanently records the first device assignment and rejects reuse on another device.
- Licensing state is separate from school backup/restore and encrypted with Windows secure storage. No school database migration or reset is required.
- See [LICENSING.md](LICENSING.md) for issuance instructions and offline enforcement limitations.

# Release 1.0.1 — startup recovery fix

- Fixed reopening getting stuck on “Another database operation is running.” Startup backup and UI requests now share a FIFO queue instead of rejecting overlapping requests.
- Failed operations release the queue so later requests continue normally.
- Added Retry controls to the initial workspace and records-loading screens.
- Normal application shutdown drains queued database work before disconnecting SQLite.
- Added a real close/reopen regression test with a delayed automatic backup, concurrent startup requests, and the same existing database across both launches.
- Automated suite: 35 passing tests. No database schema change or data reset is required.

# Release 1.0.0 — release candidate

## Included

Offline Electron desktop workflow; React/TypeScript UI; normalized Prisma/SQLite records; salted local passwords; six roles with configurable action restrictions; assigned-class permissions; student profiles and history; enrollment; attendance; assessment scoring; grade approval/locking; promotion; permanent-record corrections; internal report previews/PDFs; native printing integration; backup/restore; audit logs; per-school-year grading policies; and Windows NSIS/portable packaging.

## Verification

- TypeScript and production renderer/Electron build.
- Vite development renderer bootstrap passed with a development-only CSP allowance for React refresh; production retains its stricter CSP.
- 32 passing unit/integration tests, including decimal grading, rounding, transmutation, missing scores, promotion, attendance and validation.
- Real SQLite integration tests for fresh setup, password changes, authentication, student CRUD/archive, enrollment, closed years, roles/assignment restrictions, administrator permission changes, school-year policy isolation, grade submission/approval/unlock, complete promotion/permanent-record correction, five report types, spreadsheet round-trip, and backup/restore.
- Electron desktop test signs in through the UI, turns network emulation offline, creates and approves synthetic class records, visits 16 module pages, checks the preload bridge/Node isolation, enumerates Windows printers, and writes five A4 report PDFs plus screenshots.
- The current production dependency audit reports no known npm advisories after dependency updates. This is not a comprehensive independent security audit.
- Packaged executable tested with the explicitly bundled generated Prisma client and native query engine. A packaging omission found during testing was corrected before delivery.
- NSIS silent installation completed with exit code 0 in a separate workspace installation directory; the installed executable passed the same offline workflow/PDF smoke test. Test host OS build: Windows x64 10.0.26200. Windows 10 was not separately tested.
- Portable executable returned exit code 0 after the isolated offline test. Its persistent test database is inspected separately because the portable launcher runs inside a temporary extraction directory.

Artifacts from the desktop test are in `test-results/desktop-smoke.json`, `test-results/dashboard.png`, and `test-results/SF*.pdf` / `SF*.png`.

## Remaining release gates

Official form template implementation and school acceptance; curriculum-specific policy approval; physical printer acceptance; Windows 10 testing; publisher code signing; optional encrypted backups. See the main README for implementation limits. This release must not be represented as fully satisfying every feature of the original production specification.
