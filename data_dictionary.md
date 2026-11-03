# Data dictionary

This document describes the contents of the CSV files in this folder. Types,
row counts, and missing-value counts are based on the files currently stored
here. A blank CSV field is treated as missing.

## File summary

| File | Rows | Columns | Record |
|---|---:|---:|---|
| `master_dataset.csv` | 3,500 | 51 | One student |
| `transcripts.csv` | 91,398 | 15 | One student-course-semester record |

`student_id` identifies a student in both files. The values are eight-digit
numeric identifiers. `student_name` is repeated for each transcript record.

## `master_dataset.csv`

All columns have 3,500 records unless a missing count is shown.

| Column | Type | Missing | Description |
|---|---|---:|---|
| `student_id` | Integer-formatted identifier | 0 | Student identifier. |
| `student_name` | Text | 0 | Student name. |
| `year_group` | Integer | 0 | Student year-group value. |
| `gender` | Text | 0 | Recorded gender category. |
| `nationality_category` | Text | 0 | Nationality category. |
| `home_region` | Text | 0 | Home-region category. |
| `high_school_curriculum` | Text | 0 | Secondary-school curriculum category. |
| `first_generation_college` | Text | 0 | First-generation college indicator. |
| `scholarship_tier` | Text | 0 | Scholarship or funding category. |
| `residential_status` | Text | 0 | Residential-status category. |
| `major` | Text | 0 | Academic major. |
| `entry_academic_index` | Decimal | 0 | Entry academic index. |
| `semesters_completed` | Integer | 0 | Number of completed semesters. |
| `graduation_semesters` | Integer | 2,157 | Number of semesters at graduation, where applicable. |
| `units_attempted` | Decimal | 0 | Total attempted course units. |
| `units_earned` | Decimal | 0 | Total earned course units. |
| `unit_completion_ratio` | Decimal | 0 | Earned units divided by attempted units. |
| `grade_engineering_calculus` | Decimal | 0 | Grade-point value for Engineering Calculus, where recorded. |
| `grade_computer_programming` | Decimal | 1,264 | Grade-point value for Computer Programming, where recorded. |
| `grade_principles_of_economics` | Decimal | 1,553 | Grade-point value for Principles of Economics, where recorded. |
| `grade_intro_engineering` | Decimal | 2,408 | Grade-point value for Introduction to Engineering, where recorded. |
| `failed_courses_count` | Integer | 0 | Count of failed course records. |
| `repeated_courses_count` | Integer | 0 | Count of repeated course records. |
| `gpa_year1` | Decimal | 0 | Year 1 GPA. |
| `gpa_year2` | Decimal | 1,026 | Year 2 GPA, where recorded. |
| `gpa_year3` | Decimal | 1,584 | Year 3 GPA, where recorded. |
| `gpa_year4` | Decimal | 1,613 | Year 4 GPA, where recorded. |
| `cumulative_gpa` | Decimal | 0 | Current or final cumulative GPA. |
| `gpa_trajectory_slope` | Decimal | 0 | GPA trajectory slope value. |
| `max_gpa_drop` | Decimal | 0 | Maximum recorded consecutive GPA decrease. |
| `weekly_self_study_hours` | Decimal | 0 | Weekly self-study hours. |
| `class_attendance_rate` | Decimal | 0 | Class attendance percentage. |
| `canvas_weekly_active_days` | Decimal | 0 | Average weekly active days on Canvas. |
| `canvas_ontime_submission_rate` | Decimal | 0 | On-time submission percentage. |
| `canvas_submission_lead_time_hours` | Decimal | 0 | Submission lead time in hours. |
| `canvas_discussion_posts_per_term` | Integer | 0 | Discussion posts per term. |
| `academic_support_visits` | Integer | 0 | Academic-support visits. |
| `advising_touchpoints` | Integer | 0 | Advising touchpoints. |
| `leadership_roles_count` | Integer | 0 | Leadership roles count. |
| `clubs_active_count` | Integer | 0 | Active clubs count. |
| `community_service_hours` | Integer | 0 | Community-service hours. |
| `internships_completed` | Integer | 0 | Completed internships count. |
| `campus_employment_hours_weekly` | Integer | 0 | Weekly campus-employment hours. |
| `latent_archetype` | Text | 0 | Assigned latent-profile label. |
| `outlier_flag` | Integer | 0 | Outlier indicator. |
| `ever_academic_probation` | Integer | 0 | Indicator for any recorded academic probation. |
| `current_academic_standing` | Text | 0 | Current academic-standing label. |
| `consecutive_probation_semesters` | Integer | 0 | Consecutive probation-semester count. |
| `academic_dismissal_flag` | Integer | 0 | Academic-dismissal indicator. |
| `completion_status` | Text | 0 | Completion-status label. |
| `early_warning_risk_tier` | Text | 0 | Early-warning risk category. |

### Observed categorical values

The following columns contain categorical text values. The listed values are
the distinct values observed in the current file.

| Column | Values |
|---|---|
| `gender` | `Female`; `Male` |
| `first_generation_college` | `Yes`; `No` |
| `outlier_flag`, `ever_academic_probation`, `academic_dismissal_flag` | `0`; `1` |
| `residential_status` | `On-Campus (Residence Halls)`; `Off-Campus (Berekuso Hostels)` |
| `early_warning_risk_tier` | `Low Risk`; `Medium Risk`; `High Risk` |

Other categorical columns contain labels in the current data. Their values
should be read directly from the CSV rather than inferred from this document.

## `transcripts.csv`

All columns have 91,398 non-missing records.

| Column | Type | Description |
|---|---|---|
| `student_id` | Integer-formatted identifier | Student identifier. |
| `student_name` | Text | Student name. |
| `degree_programme` | Text | Degree-programme label. |
| `major` | Text | Academic major. |
| `academic_year` | Integer | Academic year value. |
| `academic_level` | Text | Academic-level label. |
| `semester` | Text | Semester label. |
| `course_title` | Text | Course title. |
| `grade` | Text | Course grade label. |
| `unit` | Decimal | Course unit value. |
| `semester_units_earned` | Decimal | Units earned in the semester. |
| `semester_gpa` | Decimal | Semester GPA. |
| `cumulative_units_earned` | Decimal | Cumulative units earned. |
| `cumulative_gpa` | Decimal | Cumulative GPA. |
| `academic_standing` | Text | Academic-standing label for the record. |

### Observed transcript values

The `grade` column contains `A+`, `A`, `B+`, `B`, `C+`, `C`, `D+`, `D`, `E`,
and `P`. The `unit` column contains decimal course-unit values, including
`0.0`, `0.5`, and `1.0`.
