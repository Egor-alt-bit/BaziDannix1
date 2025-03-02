Шпаргалки по базам данных

1.SELECT - выбирает отдельные столбцы или всю таблицу целиком

Пример:
SELECT column1, column2, ...
FROM table_name;

На этом примере показано как этой командой выбрали два поля таблицы (column) из таблицы (table)
Проще говоря с помощью этой команды мы выбираем элементы таблицы

2.UPDATE - команда с помощью которой мы обновляем данные в таблице или ее отдельных частях

Пример:
UPDATE table_name
SET column1 = value1, column2 = value2, ...

На этом примере показано как с помощью update мы указали таблицу(table) и также указываем столбцы и новые значения для них

3.WHERE - команда точнее условие по которому sql выбирает данные

Пример:
SELECT (Name, Age) FROM Clients WHERE Age > 20

На этом примере мы с помощью этого условия выделили условие для нашего запроса т.е клиенты с возрастом больше 20 лет

4.And и Or - это операторы для составления условий 

Пример And:
SELECT * FROM table_name WHERE fname='Ivan' AND lname='Abrakov';

На этом примере выборка (SELECT) записи, где поле fname равно 'Ivan' AND(и) поле lname равно 'Abrakov'.

Пример Or:
SELECT * FROM table_name WHERE fname='Ivan' OR fname='Alex';

На этом примере выборка (SELECT) записи, где поле fname равно 'Ivan' OR(или) поле fname равно 'Alex'.

5.Order by - команда с помощью которой мы можем сортировать данные

Пример:
SELECT поля_таблиц FROM наименование_таблицы
WHERE ...
ORDER BY столбец_1 [ASC | DESC][, столбец_n [ASC | DESC]]

У Order by есть свои условия ASC и DESC

ASC - упорядочивание по возрастанию
DESC - упорядочивание по убыванию

6.Delete - команда, точнее оператор с помощью которого мы можем удалять записи из таблицы

Пример:
DELETE FROM имя_таблицы
[WHERE условие_отбора_записей];

На этом примере мы сначало с помощью where задали условие, а потом с помощью оператора удалили записи по этим условиям

7.LIMIT и OFFSET - Операторы для выборки

Пример LIMIT:
SELECT * FROM products 
ORDER BY price DESC 
LIMIT 5

Оператор Limit позволяет нам выделить то количество данных которое нам нужно, т.е допустим количество файлов 10, но с помощью limit мы выделяем и выводим всего 5, как и показано на примере

Пример OFFSET:
SELECT ProductID, ProductName, Category
FROM Products
ORDER BY ProductName
LIMIT 3 OFFSET 3;

Оператор OFFSET позволяет пропустить некое количество строк, как показано на примере мы с помощью него пропустили 3 строки и вывели только 3 следующие после пропущенных

8.Set - эта команда плотно работает с update с её помощью мы выбираем столбец и значение для обновления

Пример:
UPDATE Customers
SET ContactName='Juan'
WHERE Country='Mexico';

На этом примере мы с помощью команды set выбрали поле ContactName и изменили на Juan с условием

9.Insert - это команда, которая используется для добавления новых записей в таблицу базы данных.

Пример:
INSERT INTO название_таблицы (список_столбцов)
VALUES (значения_столбцов);

На этом примере показан синтаксис этой команды, где INSERT INTO означает "добавить в", а командой VALUES мы задаем значение, т.е мы с помощью этой команды добавляем данные в таблицу

10.Truncate - это команда которая удаляет все строки в таблице или указанные секции таблицы, не записывая в журнал удаление отдельных строк.

Пример:
TRUNCATE TABLE Geroev

На этом примере я удалил все данные из таблицы со своей фамилией





