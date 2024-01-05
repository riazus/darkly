# 03_iamges_sql_injection

## Instruction

Using this query we can notice interesting comment of image with id=5

```
1 AND 1=2 UNION SELECT id, comment FROM Member_images.list_images
```

## How to prevent

Should I really repeat every time that ORMs more secure than direct SQL usage?
Btw, of course if the circumstances doesn't allow using ORM, we can write own checkers, but this solution is much worse than ORMs
