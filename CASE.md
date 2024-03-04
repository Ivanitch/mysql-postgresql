## MySQL

Выражение `CASE` проверяет условия и возвращает значение при выполнении первого условия.

```sql
SELECT 
CASE
    WHEN condition1 THEN 'result1'
    WHEN condition2 THEN 'result2'
    [ELSE else_result]
END;
```

### Примеры

```sql
SELECT
CASE
    WHEN 10 < 3 THEN '10 меньше чем 3'
    WHEN 10 > 3 THEN '10 больше чем 3' -- 10 больше чем 3
    ELSE 'default'
END
```


