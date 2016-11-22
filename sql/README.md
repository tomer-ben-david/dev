# SQL
## In same query you can refer to same table twice

```sql
select firstname, lastname 
  from names as a,
       names as b
  WHERE a.firstname = b.firstname
    AND a.lastname != b.lastname
```
