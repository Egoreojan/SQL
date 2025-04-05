### Добавление записи в таблицу

Пример запроса:

````sql
INSERT INTO positions (id, title, salary) VALUES
	('1', 'Программист', '1500'),
	('2', 'Юрист', '700'),
	('3', 'HR', '700'),
	('4', 'Дизайнер', '700'),
	('5', 'Маркетолог', '500'),
	('6', 'Data Engineer', '3000');

INSERT INTO persons (id, name, position_id) VALUES
    ('1', 'Владимир', '4'),
    ('2', 'Алёна', '1'),
    ('3', 'Евгений', '5'),
    ('4', 'Артём', '2'),
    ('5', 'Борис', '4'),
    ('6', 'Татьяна', '3');
````

Расшифровка `ВСТАВЬ В (таблицу)  positions в столбцы( id, title, salary) ЗНАЧЕНИЯ (...)`

### Обновление записи в таблице

````sql
UPDATE positions
SET title = 'Халтурщик', salary = '50'
WHERE id = 7;
````

### Удаление записи в таблице

````sql
DELETE FROM positions
WHERE id = 7;
````

### Выборка данных (SELECT)

Общий вид:

````sql
SELECT [ ALL | DISTINCT [ ON ( expression [, ...] ) ] ]
    [ * | expression [ [ AS ] output_name ] [, ...] ]
    [ FROM from_item [, ...] ]
    [ WHERE condition ]
    [ GROUP BY [ ALL | DISTINCT ] grouping_element [, ...] ]
    [ HAVING condition ]
    [ { UNION | INTERSECT | EXCEPT } [ ALL | DISTINCT ] select ]
    [ ORDER BY expression [ ASC | DESC | USING operator ] [ NULLS { FIRST | LAST } ] [, ...] ]
    [ LIMIT { count | ALL } ]
    [ OFFSET start [ ROW | ROWS ] ]
    [ FETCH { FIRST | NEXT } [ count ] { ROW | ROWS } { ONLY | WITH TIES } ]
    [ FOR { UPDATE | NO KEY UPDATE | SHARE | KEY SHARE } [ OF table_name [, ...] ] [ NOWAIT | SKIP LOCKED ] [...] ]
````

````sql
SELECT название_столбца1, название_столбца2, название_столбцаN 
FROM название_таблицы;
````

Пример:
````sql
SELECT * 
FROM positions;
````

Чтобы выбрать все столбцы:
````sql
SELECT * 
FROM название_таблицы;
````

#### Фильтрация выборки (WHERE)

````sql
SELECT title
FROM positions
WHERE salary > 1000;
````