## MySQL

Функция `COALESCE()` возвращает первый элемент списка не равный `NULL`.

### Примеры

```sql
SELECT COALESCE(NULL, NULL, 1, 2); -- 1
```

```sql
SELECT first_name, last_name,
    COALESCE(phone, email, 'не определено') AS contcts
FROM client;
```





