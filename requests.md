## Basic MySQL requests:
___
- *Показать доступные базы данных:*
    ```sql
     SHOW DATABASES;
     ```
- *Показать список таблиц в текущей базе данных:*
    ```sql
    SHOW TABLES;
    ```
- *Использовать выбранную базу данных:*
    ```sql
    USE db_name;
    ``` 
- *Выводит все записи и все строки таблицы **table_name**:*
    ```sql
    SELECT * FROM table_name;
    ```
- *Выводит только **id** из таблицы **table_name**:*
    ```sql
    SELECT id FROM table_name;
    ```
- *Выводит только **name** из таблицы **table_name**:*
    ```sql
    SELECT name FROM table_name;
    ```
- *Выводит только **email** из таблицы **table_name**:*
    ```sql
    SELECT email FROM table_name;
    ```
- *Выводит **name** и **email** из таблицы **<table_name>**:*
    ```sql
    SELECT name, email FROM table_name;
    ```
- *Выводит **id**, **name**, **email** и **created_on** из таблицы **table_name**:*
    ```sql
    SELECT id, name, email, created_on FROM table_name;
    ```
- *Выводит все записи из таблицы **table_name**, где password = 0000:*
    ```sql
    SELECT * FROM table_name WHERE password = '0000';
    ```
- *Выводит все записи из таблицы **table_name**, которые были созданы в указанную дату (YEAR-MM-DD 00:00:00):*
    ```sql
    SELECT * FROM table_name WHERE created_on = 'YEAR-MM-DD 00:00:00';
    ```
- *Выводит все записи из таблицы **table_name**, где в **name** есть совпадение **match**:*
    ```sql
    SELECT * FROM table_name WHERE name LIKE '%match%';
    ```
- *Выводит все записи из таблицы **table_name**, где в **name** в конце есть совпадение **es**:*
    ```sql
    SELECT * FROM <table_name> WHERE name LIKE '%es';
    ```
- *Выводит все записи из таблицы **table_name**, где в **name** в начале литера **'а'**:*
    ```sql
    SELECT * FROM table_name WHERE name LIKE 'a%';
    ```
- *Выводит все записи из таблицы **table_name**, которые были созданы в указанную дату (YEAR-MM-DD 00:00:00):*
    ```sql
    SELECT * FROM table_name WHERE created_on = 'YEAR-MM-DD 00:00:00';
    ```
- *Выводит все записи из таблицы **table_name**, которые были созданы в указанную дату (YEAR-MM-DD 00:00:00) и имеют **password** = 0000:*
    ```sql
    SELECT * FROM table_name 
             WHERE created_on = 'YEAR-MM-DD 00:00:00'
             AND password = '0000';
    ```
- *Выводит все записи из таблицы **table_name**, которые были созданы (YEAR-MM-DD 00:00:00) и у которых в **name** есть совпадение **request**:*
    ```sql
    SELECT * FROM table_name
             WHERE created_on = 'YEAR-MM-DD 00:00:00'
             AND name LIKE '%request%';
    ```
- *Выводит все записи из таблицы **table_name**, которые были созданы (YEAR-MM-DD 00:00:00) и у которых в **name** есть цифра **0**:*
    ```sql
    SELECT * FROM table_name 
             WHERE created_on = 'YEAR-MM-DD 00:00:00'
             AND name LIKE '%0%';
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** равен **9**:*
    ```sql
    SELECT * FROM table_name WHERE id = 9;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** больше **1**:*
    ```sql
    SELECT * FROM table_name WHERE id > 1;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** меньше **10**:*
    ```sql
    SELECT * FROM table_name WHERE id < 10;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** меньше **3** или больше **6**:*
    ```sql
    SELECT * FROM table_name WHERE id < 3 OR id > 6;;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** меньше либо равно **5**:*
    ```sql
    SELECT * FROM table_name WHERE id <= 5;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** больше либо равно **7**:*
    ```sql
    SELECT * FROM able_name WHERE id >= 7;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** больше **4**, но меньше **8**:*
    ```sql
    SELECT * FROM table_name
             WHERE id > 4 AND id < 8;
    ```
- *Выводит все записи из таблицы **table_name**, у которых **id** между **1** и **9**:*
    ```sql
    SELECT * FROM table_name
             WHERE id 
             BETWEEN 1 AND 9;
    ```
- *Выводит все записи из таблицы **table_name**, где **password** равен **0000**, **'start1'**, **'_hello'**:*
    ```sql
    SELECT * FROM table_name
             WHERE password 
             IN ('0000', 'start1', '_hello');
    ```
- *Выводит все записи из таблицы **table_name**, где **created_on** равен указанным датам (YEAR-MM-DD 00:00:00, YEAR-MM-DD 12:00:00, YEAR-MM-DD 24:00:00):*
    ```sql
    SELECT * FROM table_name 
             WHERE created_on
             IN ('YEAR-MM-DD 00:00:00','YEAR-MM-DD 12:00:00','YEAR-MM-DD 24:00:00');
    ```
- *Выводит максимальный **id** из таблицы **table_name**:*
    ```sql
    SELECT MAX(id) FROM table_name;
    ```
- *Выводит минимальный **id** из таблицы **table_name**:*
    ```sql
    SELECT MIN(id) FROM table_name;
    ```
- *Выводит **count** (количество) всех записей из таблицы **table_name**:*
    ```sql
    SELECT COUNT(*) FROM table_name;
    ```
- *Выводит **id**, **name**, **created_on**из таблицы **table_name** и сортирует по порядку возрастания **created_on**:*
    ```sql
    SELECT id, name, created_on FROM table_name 
                                ORDER BY created_on;
    ```
- *Выводит **id**, **name**, **created_on**из таблицы **table_name** и сортирует по порядку убывания **created_on**:*
    ```sql
    SELECT id, name, created_on FROM table_name
                                ORDER BY created_on DESC;
    ```
- *Выводит все записи **name** из левой таблицы (**table_name1**) и соответствующие записи **name** из правой таблицы (**table_name2**). Результат равен 0 записей **name** из **table_name2**, если совпадений нет:*
    ```sql
    SELECT name FROM table_name1
                LEFT JOIN table_name2
                ON table_name1.name = table_name2.name;
    ```
- *Выводит все записи **name** из правой таблицы (**table_name2**) и соответствующие записи **name** из левой таблицы (**table_name1**). Результат равен 0 записей **name** из **table_name1**, если совпадений нет:*
    ```sql
    SELECT name FROM table_name1 
                RIGHT JOIN table_name2
                ON table_name1.name = table_name2.name;
    ```
