# Installation and first use

## Windows setup

1. Download and run `GuroDesk.Setup.1.9.0.exe` from the [latest release](https://github.com/rxbytecom/GuroDesk/releases/latest).
2. Choose an installation directory and complete the installer.
3. Launch **GuroDesk** from the Start menu or desktop shortcut.
4. Complete the school profile, school year, and administrator credentials.
5. Add Teacher and Adviser accounts under Users. Add subjects and their policy-specific weights.
6. Create sections, assign advisers, then add subject/teacher assignments.
7. Review and approve the applicable school-year policy under Settings.
8. Add/import learners, enroll them, record attendance, and create assessments.
9. Enter every required score, submit the class record, and sign in with an authorized administrator to approve it.
10. Calculate promotion after all required grading periods and subjects have approved grades.

First-run setup creates grade levels Kindergarten through Grade 12; sections remain empty until configured. Selecting a school year in the header refreshes the corresponding records. Closing a year prevents ordinary enrollment, attendance, and academic changes; authorized permanent-record corrections retain an audit trail.

## Data location

Installed application: `%APPDATA%\deped-smart-school\school.db` (Electron's per-user application-data directory). Backups created automatically are in its `backups` subfolder. Development: `<repository>\.data\development.db`.

The portable executable uses the same per-user data model; it is not a USB-contained database. Installation upgrades replace program files and retain user data.

## Uninstalling

Starting with version 1.1.1, uninstalling through Windows removes the current Windows user's `%APPDATA%\deped-smart-school` folder, including the school database, stored attachments, automatic and pre-restore backups, database recovery files, settings, logs, and browser cache. This is permanent file deletion, not a secure disk wipe. Save any backup you need outside that folder before uninstalling. Normal version upgrades preserve this data.

Manual backups, exported PDFs/spreadsheets/documents saved elsewhere, other Windows users' profiles, developer/test data directories, are not deleted. Deleting a portable executable alone does not run an uninstaller or remove its data. Install this version first to replace the older data-preserving uninstaller.

Reinstalling after a full uninstall starts a fresh, empty workspace. GuroDesk is free and needs no activation.

`SMART_SCHOOL_DATA_DIR` is a developer/test override for the database directory. Do not point different running installations at the same SQLite file. Close the application before manually moving its database.

## Imports

Export a workbook from Student Profiling to obtain the column names. XLSX and CSV imports use the first sheet/header row and add new students only. Required headers:

```csv
lrn,firstName,lastName,sex,birthdate,guardian
123456789012,Sample,Learner,Female,2013-06-10,Sample Guardian
```

Dates must be `YYYY-MM-DD`, sex `Male` or `Female`, and LRN exactly 12 digits. Format LRN cells as text in spreadsheets to preserve leading zeros. An invalid row, duplicate LRN, or existing LRN rejects the import. A native confirmation shows the validated row count before all rows are saved in one transaction.

## Larger text

Use the **Text size** toolbar at the top of the app. Choose **125% Large**, **150% Extra large**, **175% Bigger**, or **200% Largest**, or press **A+** / **A−**. **Reset** returns to 100%. These controls also work before sign-in. Use Tab to reach the controls and arrow keys to change the selection.

The setting is remembered on the current Windows profile, including after closing and reopening. People using the same Windows profile share this preference. It affects application text; generated forms and PDFs keep their prescribed font sizes. At larger sizes some panels stack vertically and tables can be scrolled horizontally.

## Printing forms

Open Forms & Reports, select the report type, grade level, and template. Select a class and learners, then Generate report. Inspect the preview and choose Preview, PDF, or Print. Each template fixes its paper size, orientation, and 6 mm margins. Match A4, Legal (8.5 × 14), or Folio (8.5 × 13) paper in the printer. Blank page range means all pages; `1-3,5` selects those pages. Learner reports and class continuations insert page breaks.

Use **Save original Excel template** to complete missing fields using the published source workbook, even offline. It contains the original source content, not your school records; review/remove any source sample entries. The native Windows dialog lets you confirm printer settings. Physical printing depends on installed printer drivers. App-generated reports are not LIS-issued documents. See [template choices and fields needing completion](POLICY-SOURCES.md).
