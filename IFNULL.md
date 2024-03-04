## MySQL

Функция `IFNULL()` возвращает значение, переданное 1-ым аргументом, если оно не равно `NULL`. В противном случае, возвращает значение переданное 2-ым аргументом.

```sql
IFNULL(value, alternative_value)
```

`value` - Возвращаемое значение, если оно не равно `NULL`

`alternative_value` - Альтернативное значение, если значение в первом аргументе было `NULL`

### Примеры
```sql
SELECT IFNULL(NULL, 'Alternative value'); -- Alternative value
```



