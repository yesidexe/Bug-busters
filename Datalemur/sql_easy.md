# Easy

### Data Science Skills

[Ejercicio](https://datalemur.com/questions/matching-skills), una empresa quiere contratar un profesional que sepa de Python, Tableau, y PostgreSQL, entonces nos dan una lista con dos columnas, skill y candidate_id, la idea es encontrar al candidato que sepa de estas tres y ordenar los candidatos de manera ascendente según el candidate_id.

```sql
SELECT candidate_id FROM candidates
WHERE skill IN ('Python','Tableau','PostgreSQL')
group by candidate_id
having count(candidate_id)=3
ORDER BY candidate_id ASC
```

### Page With No Likes

[Ejercicio](https://datalemur.com/questions/sql-page-with-no-likes)

```sql

```