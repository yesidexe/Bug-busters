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

[Ejercicio](https://datalemur.com/questions/sql-page-with-no-likes), nos dan dos tablas, la primera es `pages` que contiene `page_id` y `page_name`, esta tabla nos muestra la página con su id y su nombre. La segunda es `page_likes`, que contiene `user_id`, `page_id` y `liked_date`, esta tabla nos muestra el id de usuario la página y la fecha en que le dio like. Nos piden mostrar las páginas a las que los usuarios no le dieron like, entonces básicament es hacer un left join y las páginas donde los campos de `page_likes` salga null, significa que son páginas sin likes, y eso lo mostramos.

```sql
select pages.page_id from pages
left join page_likes 
on pages.page_id = page_likes.page_id
where liked_date is null
order by pages.page_id DESC
```

### Unfinished Parts
[Ejercicio](https://datalemur.com/questions/tesla-unfinished-parts)