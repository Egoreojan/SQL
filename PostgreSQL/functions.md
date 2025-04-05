## Функции SQL

### Дата

`TIMEDIFF(time_max, time_min)` - получает разницу между датами в формате `HH:MM:SS`

````sql
SELECT town_to, TIMEDIFF(time_in, time_out) as flight_time
FROM Trip
WHERE town_from = "Paris";
````

`YEAR(DATE)` - получает год из даты

````sql
SELECT * FROM Student
WHERE YEAR(birthday) IN (2000, 2002, 2004);
````