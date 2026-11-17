# Subject grading and report cards

## Choose how each subject is graded

Open **Subjects ? Edit subject**, or choose a class/subject in **E-Class Record ? Subject grading settings**. These controls require catalog permission in Multi-User Mode and are available in Single-User Teacher Mode.

Each subject has its own entry method and Written Works / Performance Tasks / Quarterly Assessment weights:

- **Calculate from activity scores:** enter scores and maximum points. The app uses this subject's weights, then the school-year grading conversion configured in Settings.
- **Enter grading-period grades directly:** enter the finished period grade, such as Mathematics 88. Direct grades must be whole numbers from 0 to 100 and are used as entered; no weighting or conversion is applied again.

Choose the method before adding assessments or grades. Once records exist, the method is protected to prevent mixing direct grades and calculated scores. Existing subjects continue to use activity scores. Settings apply to all classes using that subject; other subjects keep their settings. Weights must total 100%, including when retained for a direct-entry subject.

## Enter grades directly

1. Select the class/subject and period in **E-Class Record**.
2. Enter the grade beside each learner. Enter moves to the next learner; Shift+Enter moves back.
3. Leave missing grades blank. Zero is an actual grade.
4. Click **Save grades to report cards** in Teacher Mode, or **Save draft grades** in Multi-User Mode.
5. Open **Report cards**. The preview loads automatically for the chosen grade level and learners.

## Enter activity scores

1. Choose the class/subject and grading period.
2. Add an assessment with its title, category and maximum score.
3. Select the activity, enter scores, then click **Save scores**.
4. Repeat for every required activity. The app shows incomplete grades until all required scores are saved.
5. Open **Report cards** to see the latest published grades.

Save or discard changes before switching activities, subjects or periods. Save before leaving the entry page. Detailed calculations remain expandable.

## When grades appear on report cards

**Single-User Teacher Mode:** review and approve the school-year grading policy in Settings once. Saving a direct grade publishes that learner's grade immediately. Saving activity scores automatically publishes each complete calculated grade. Incomplete grades remain blank. Corrections are recorded in the audit history; clearing a saved grade or required score removes that period grade from newly generated cards. Records remain editable while the school year is open.

If the policy is not yet approved, saves remain drafts. Approving the policy in Settings publishes every complete calculated grade automatically; no re-saving is needed. Changing a subject's weights or the grading policy later recalculates saved activity-score grades automatically (Teacher Mode, or Draft grades in Multi-User Mode). Learners with promotion decisions or permanent records keep their recorded grades.

**Multi-User / Admin Mode:** save drafts, submit the complete class, then have an authorized reviewer approve it in **Grades**. Only approved grades appear on report cards. Submitted/approved records remain locked until returned/unlocked. Existing teacher assignments and permissions still apply.

Opening **Report cards** generates a fresh preview automatically, with saved approved grades matched by learner, class, subject and grading period. Choose the correct grade level, section and learners. Previous PDF/printed copies do not change; export or print a new copy after corrections. The Readable layout lists assigned subjects. Published templates must match the subject rows and number of grading periods; check the preview notices for unsupported combinations.

## DepEd DO 015, s. 2026 setup (one click)

New installations start with the DO 015, s. 2026 values: three terms, passing grade 75 and the adjusted transmutation table (initial grade 70.00 → 75; minimum reportable grade 60). Existing schools can open **Settings → Grading & promotion policy** and click **Use DepEd DO 015, s. 2026 (SY 2026–2027)**, review the table, tick approval and save.

Subject weights fill in automatically: leave the three weight fields blank when adding or editing a subject. English, Filipino, Mathematics, Science, Araling Panlipunan and GMRC/Values Education use 20/50/30 (Written or Oral Works / Product or Performance Tasks / Examinations). EPP/TLE and MAPEH use 20/60/20, SHS TechPro electives 15/65/20, Research 40/60/0 and Work Immersion 20/80/0. **Subjects → Apply DepEd weights to all subjects** updates the whole catalog at once.

When adding an assessment, choose **Summative Test 1**, **Summative Test 2** or **Term Examination** for the Examinations component. The app combines them as 30% / 30% / 40%. Titles are optional; untitled activities are numbered automatically.

## Calculation details

For each category, total earned points / total possible points ? category weight gives the weighted score. The app adds those scores and applies the configured school-year conversion (table, linear, or identity). These formulas are unchanged.

The final subject grade averages all required grading periods, rounding half up. Missing periods remain incomplete. Promotion still uses the school's configured and approved policy.

## Published forms with different grading fields (1.7.1)

When the published SF9 cannot represent the configured periods or subjects, a **Saved subject grades** supporting page follows the original form. Scroll through the preview/PDF to see it. This includes four-period years using three-term forms, descriptive early-grade cards and semester-specific SHS cards. All saved approved period grades appear with their actual period names; the original official fields remain unchanged. SF10 also includes current-year approved period grades as a separate supporting record, without substituting them for verified historical/semester entries.

Compatible three-term grades still fill matching SF9 cells. Direct and calculated grades follow the same approval rules. If no approved grades exist, the preview explains pending approval instead of printing unapproved grades. Existing PDF files must be exported again.

## Main table and age (1.7.2)

In Published SF9, **Main grade table periods** selects the saved period to copy into each T1/T2/T3 column. The first three saved periods are selected by default, even when the school year uses four. Change these selectors if your school requires a different mapping, or select Leave blank. A fourth period remains on the supporting page. The values are copied as saved, not converted into semester/term results. Final Grade still uses all periods required by the grading policy.

**Age as of** defaults to today and can be changed to the school's reference date. The app calculates completed years from the student's saved birthdate. Fix a missing or incorrect birthdate in Student Profiling. Age remains blank if the birthdate is invalid or later than the reference date. Reopen Report cards or regenerate an existing report after changes.

## Subject names in report cards

Report cards use the subjects assigned to the learner?s class under Classes & sections, not every subject in the school catalog. In Subjects, choose Show subjects for class to check this list.

Published numeric SF9 cards keep the learning areas printed on the official DepEd form (for example, Grade 2: Filipino, English, Mathematics, GMRC / Values Education and Makabansa). A subject's grades print in the row with the same name; use Report row to link a differently named subject, such as Edukasyon sa Pagpapakatao to GMRC / Values Education. Only SHS elective rows (Academic/TechPro Elective) take the subject's own name. Subjects without a matching row never replace an official learning area; they appear on the supporting page. Remarks follow the form rule: 75 and above is Passed. Grey-shaded elective terms stay blank. Only approved grades print; unsaved or unapproved grades remain blank.

Semester cards show the assigned names but do not convert grading-period values to semester grades. Competency forms and verified historical SF10 records keep their distinct content; supporting pages show current assigned subjects and numeric grades. Regenerate old reports to update them.

## Deleting records

Use Delete beside the item and review the confirmation before choosing Confirm delete. In E-Class Record, select an activity to delete that activity and its scores; direct-grade rows have individual delete buttons. Grades also has individual saved-grade deletion. Activity scores remain when only a saved grade is deleted, and submitting or saving them later can recreate that grade. Regenerate report previews and exports after deletions.

Parents with linked school records cannot be deleted. Remove unused subject assignments before deleting a subject or section. A learner with enrollment history should be archived instead. Multi-User submitted/approved grades require return/unlock; closed years and finalized promotion/permanent records remain protected. Deletions are logged, and previous report copies remain unchanged.


### SF10 subjects and learner details

Regenerate SF10 after changing student details or class subject assignments. Current-year scholastic sections use the learner?s class assignments; finalized historical sections retain their saved subject names and final ratings. Only approved grades are displayed. Four quarterly columns are populated only for a four-period policy; other saved periods remain on the supporting grade page. Semester grades, track categories and passing status are not inferred from assignment alone. Senior-high subjects outside the template catalog appear under Other Subjects in the annex. Existing published files are snapshots and must be regenerated.
