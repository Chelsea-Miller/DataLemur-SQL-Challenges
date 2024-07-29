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
## Page With No Likes

Question Source: https://datalemur.com/questions/sql-page-with-no-likes

```
SELECT pages.page_id 
FROM pages FULL OUTER JOIN page_likes on pages.page_id = page_likes.page_id
Where page_likes.page_id is NULL
order by page_id;
```
