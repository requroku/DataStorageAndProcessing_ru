# Упражнение 4
Этот элемент курса оценивается как 'Упражнение 4'
вес: 1.0

Составьте правильные запросы из представленных фрагментов (учтите, что некоторые фрагменты могут быть лишними!), исполните эти запросы к тестовой базе данных **STUDENT&TEST**. [Воспользуйтесь инструкцией по доступу к тестовой базе данных](#) и [описанием БД](./data/Описание_базы_Student.pdf).

В соответствующие поля введите как сам запрос, так и полученный ответ.


## Задача 1
Фрагменты: `Test_ID=4` `WHERE` `SELECT` `FROM` `INCLUDE` `Test_Name_Ru` `TEST`

Как называется упражнение 4? Ответ выведите на русском языке.

Введите запрос:  
```sql
select test_name_ru from test where test_id=4
```

Введите результат запроса:  
```sh
Цифровая этика
```


## Задача 2
Фрагменты: `Test_ID=8` `SELECT` `WHERE` `AND` `COUNT(*)` `STUDENT_TEST` `EXISTS` `Score=100` `FROM` `OR`

Сколько человек получило сто баллов по упражнению 8?

Введите запрос:
```sql
select COUNT(*) from student_test where test_id=8 AND Score=100
```
Введите результат запроса:
```sh
1159
```


## Задача 3
Фрагменты: `WHERE` `FROM STUDENT_TEST` `JOIN` `UNION` `SELECT` `TEST` `ON` `STUDENT_TEST.Test_ID=TEST.Test_ID` `AVG(Score)` `Test_Name_Ru='Технологии программирования'`

Найдите средний балл по Упражнению 'Технологии программирования' по всем студентам.

Введите запрос:
```sql
SELECT AVG(Score) FROM STUDENT_TEST JOIN TEST ON STUDENT_TEST.Test_ID=TEST.Test_ID WHERE Test_Name_Ru='Технологии программирования'
```

Введите результат запроса:  
<sub>***Ответ округлите до целого числа.***</sub>
```sh
89
```


## Задача 4
Фрагменты: `FROM (SELECT Student_ID` `JOIN` `GROUP BY Student_ID` `HAVING COUNT(*)=14)` `SELECT COUNT(*)` `FROM STUDENT_TEST`

Сколько человек сдали ровно 14 заданий?

Введите запрос:
```sql
SELECT COUNT(*) FROM (SELECT Student_ID FROM STUDENT_TEST GROUP BY Student_ID HAVING COUNT(*)=14)
```

Введите результат запроса:
```sh
358
```
