## MySQL

Функция `COALESCE()` возвращает первый элемент списка не равный `NULL`.

```sql
COALESCE (argument_1, argument_2, argument_3);
```

### Примеры

```sql
SELECT COALESCE(NULL, NULL, 1, 2); -- 1
```

```sql
SELECT first_name, last_name,
    COALESCE(phone, email, 'не определено') AS contcts
FROM client;
```

> Функция `COALESCE()` работает похожим образом в MySQL и PostgreSQL,

[Основные отличия между COALESCE() в MySQL и PostgreSQL](IFNULL.md#coalesce-diff)





