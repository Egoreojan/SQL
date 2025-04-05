## Функции преобразования типов, CAST

````sql
CAST(значение AS тип_для_конвертации);
CONVERT(значение, тип_для_конвертации);
````

Пример:

````sql
SELECT CAST(12005.6 AS DECIMAL), CONVERT(12005.4, DECIMAL);
````

![/assets/cast.png](/assets/cast.png)