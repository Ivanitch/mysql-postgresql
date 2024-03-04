## MySQL

Функция `IF()` возвращает значение, переданное 2-ым или 3-им аргументом, в зависимости от истинности условного выражения

```sql
IF(condition, value_if_true, value_if_false)
```
`condition` - Условное выражение

`value_if_true` - Значение, возвращаемое если условное выражение истинно

`value_if_false` - Значение, возвращаемое если условное выражение ложно

### Примеры
```sql
SELECT IF(10 > 20, '10 больше чем 20', '10 меньше чем 20'); -- 10 меньше чем 20
```

```sql
SELECT product_name, manufacturer,
    IF(product_count > 5, 'Много товара', 'Мало товара')
FROM product;
```

## PostgreSQL

В PostgreSQL нет встроенной функции `IF()`. 

В **PostgreSQL** существует несколько альтернатив функции `IF()`, которые можно использовать в зависимости от контекста и требуемого результата. Вот некоторые из них:

1) **CASE:** Это конструкция, которая позволяет выполнять условные выражения. Она состоит из нескольких частей `WHEN`, которые проверяются последовательно, и одной части `ELSE`, которая является необязательной. Например:
```sql
SELECT
    CASE
        WHEN column_name > 10 THEN 'Value is greater than 10'
        WHEN column_name = 10 THEN 'Value is equal to 10'
        ELSE 'Value is less than 10'
    END
FROM table_name;
```

2) **COALESCE:** Эта функция возвращает первое непустое значение из списка аргументов.
```sql
SELECT COALESCE(column_name1, column_name2, 'default value') FROM table_name;
```

3) **NULLIF:** Эта функция возвращает `NULL`, если два указанных значения равны, и первое значение в противном случае.

```sql
SELECT NULLIF(column_name, 'some value') FROM table_name;
```

4) **BOOLEAN expressions:** В PostgreSQL можно использовать булевские выражения для условного выбора.
```sql
SELECT column_name1 > 10 OR column_name2 IS NOT NULL FROM table_name;
```

Эти альтернативы могут быть полезны в разных ситуациях, и их можно использовать для решения различных задач.
