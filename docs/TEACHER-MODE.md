# Single-User Teacher Mode

This is an additional mode in the existing Windows application. Multi-User / Admin Mode remains the default for existing databases.

## Enable the mode

- Existing school: sign in as an administrator, open **Settings → Application Mode**, select **Single-User Teacher Mode**, and click **Apply mode**.
- New school: select **Single-User Teacher Mode** during first setup, complete the local teacher profile, and click **Open teacher workspace**. No administrator, teacher account, username, or password is created.
- Subsequent starts load the local database and open the Dashboard automatically.

## Local teacher profile

Settings contains Teacher Name, Employee ID, Position, School Name, School ID, Grade Level, Section, and School Year. This profile is saved locally, not in the user/account table. School ID uses six digits and School Year uses the existing `YYYY-YYYY` format.

The profile does not rewrite existing school records. Configure actual academic years, sections, subjects, calendar days, and the grading policy using their existing screens. School settings continue to supply the school details printed on reports. Other school information can be left blank in Teacher Mode until it is available.

## Features and mode switching

Dashboard, students, enrollment, attendance, E-Class Record, grades and grade review, forms, reports, permanent records, print/PDF, backups, and settings remain available. Account management, teacher accounts, roles, permission controls, password changes, and logout are hidden and their account operations are disabled in Teacher Mode.

Subject assignments can be created without an account in Teacher Mode. Existing adviser and teacher account links are preserved. When returning to Multi-User / Admin Mode, an administrator can assign account-free subjects to a teacher account using the existing subject assignment screen.

Select **Multi-User / Admin Mode** in Settings to restore login and account controls. Existing administrator credentials remain unchanged. If a workspace was created without any administrator, credentials are requested only when you explicitly switch to Multi-User / Admin Mode. Switching modes does not delete school records, users, or permissions.

## Storage and backups

The existing `AppSettings` table stores `application_mode` (`multi_user` or `single_user_teacher`) and `teacher_profile` (JSON). A local execution context attributes actions to `local-teacher`; it is not a user row or an authenticated account.

The migration makes the teacher-account reference on subject assignments optional, preserving assignment IDs and all existing links, assessments, scores, and grades. It runs transactionally with a foreign-key check and a pre-migration database copy. Calculations, report templates, and print layouts are unchanged.

Backups include the mode and profile. Restoring a Teacher Mode backup does not require an administrator account. Valid older backups are migrated in a staging copy before restoration. Restoring a Multi-User backup restores its login requirements.

Install the update over the existing application. Do not uninstall to update: uninstalling intentionally deletes local application data.

## Verification

- Automated integration tests cover fresh setup with zero users, account-free subject assignments, grade calculation/review, reports, teacher profile persistence, backups, restart, mode switching, and preservation of a previous multi-user database.
- Desktop tests exercise actual teacher setup and mode controls, two application launches, hidden account controls, required school routes, and PDF export for SF1, SF2, SF5, SF9, and SF10.
- Native print commands are exercised with a test callback; no physical printer output is sent.
- The existing multi-user desktop and permission tests remain in the suite.

Developer checks: `npm.cmd test`, `node scripts/smoke.mjs`, and `node scripts/teacher-mode-smoke.mjs`. Desktop test scripts use disposable databases. An optional executable argument tests the packaged application.
