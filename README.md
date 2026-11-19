# SkillGap AI – Skill Gap Matcher

Part of my Campus2Corporate idea (TechnoVate Challenge 2026).
Given a student's skills and a target role, this notebook gives a match score
and lists the skills the student is still missing.

## How it works
- Roles and their required skills are stored in a pandas table
- TF-IDF turns each skill list into numbers and cosine similarity gives the match score
- Missing skills are the role's required skills that the student does not have

## Tools
Python, pandas, scikit-learn (Google Colab)

## Limitations and next steps
- The roles table is small (12 roles) and written by hand
- Next: add more roles and real internship data
  
## Example
- Student skills: Python, SQL, pandas
- Target role: Data Analyst
- Match score: 63%
- Missing skills: excel, data visualization, statistics

## Evaluation
I tested the matcher on 10 hand-written sample student profiles (3-4 skills each).
- Top-1 accuracy: 9/10
- Top-3 accuracy: 10/10
- One miss: "linux, networking, python" was matched to Cloud Engineer instead of Cybersecurity Intern, because both roles share those skills.

Limitation: the test set is small and written by me, so this is a sanity check, not a full evaluation.

