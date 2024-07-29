## Data Science Skills

Question Source: https://datalemur.com/questions/matching-skills

My Solution:
```
select candidate_id FROM
  (SELECT candidate_id, count(*) skill_count FROM candidates
  Where skill='Python' or skill='Tableau' or skill='PostgreSQL'
  GROUP BY candidate_id) as skills
Where skill_count = 3
```
