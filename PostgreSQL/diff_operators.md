## Операторы сравнения:
- `=` - сравнение на равенство
- `<>` - сравнение на неравенство
- `!=` - сравнение на неравенство
- `<` - меньше чем
- `>` - больше чем
- `<=` - меньше чем или равно
- `>=` - больше чем или равно
- `LIKE` - сравнивает вхождение
- `IN` - проверяет значение в выборке
- `IS NULL` - проверяет на равенство `NULL`
- `BETWEEN` - Оператор `BETWEEN min AND` max позволяет узнать, расположено ли проверяемое
- значение столбца в интервале между min и max, включая сами значения min и max

Условие `LIKE` или `NOT LIKE`  позволяет использовать подстановочные символы (метасимволы) в операторе `WHERE`.
Примеры:

**LIKE**
````sql
SELECT title, salary
FROM positions
WHERE title LIKE '%Data%';
````

**BETWEEN**
````sql
SELECT room_id, start_date, end_date
FROM Reservations
WHERE total BETWEEN 500 AND 1200;
````

**IN**
````sql
SELECT * FROM Student
WHERE YEAR(birthday) IN (2000, 2002, 2004);
````