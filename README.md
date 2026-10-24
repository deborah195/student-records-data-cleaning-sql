## 1. Ask

A school's records office depends on accurate student data. These are the questions this project answers.

| # | Question (plain language) | Why it matters | How I'll answer it (technical) |
|---|---|---|---|
| 1 | How many student records can't be used to contact the student? | A missing or invalid email or phone means the school can't reach the student about deadlines or aid. | Count NULL, blank, and malformed values in the email and phone columns using SQL. |
| 2 | Which data problems affect the most records? | Fixing the biggest problems first saves the most time. | Profile each column with GROUP BY and COUNT, then rank issues by number of affected rows. |
| 3 | Do students who complete the FAFSA receive more aid? | Shows whether the financial aid process is working as expected. | JOIN the students and aid tables on student_id, then compare totals by FAFSA status. |
| 4 | Which majors have the most students receiving aid? | Helps the school see where aid is concentrated. | JOIN students and aid, GROUP BY major, and count distinct aided students. |
