**Задание 1**.
Создайте таблицу users для хранения информации о пользователях сайта. В таблице должны быть следующие поля: id – идентификатор, целое положительное; email – адрес электронной почты, строка не более 100 символов; date_joined – дата регистрации (достаточно хранить дату, без времени) last_activity – дата и время последней активности (с точностью до секунд).



![5379620308778087112](https://github.com/user-attachments/assets/f8ce234e-11c1-448b-b681-c5cc0f42d183)



Неверное решение:


```
CREATE TABLE users(
id INT UNSIGNED,
email VARCHAR(100),
date_joined DATE,
last_activity DATETIME
);

INSERT INTO users (id, email, date_joined, last_activity)
VALUES (1, "user1@domain.com", "2014-12-12", "2016-04-08 12:34:54")
INSERT INTO users (id, email, date_joined, last_activity)
VALUES (2, "user2@domain.com", "2014-12-12", "2017-02-13 11:46:53")
INSERT INTO users (id, email, date_joined, last_activity)
VALUES (3, "user3@domain.com", "2014-12-13", "2017-04-04 05:12:07")
```


Правильное решение:


```
CREATE TABLE users(
id INT UNSIGNED,
email VARCHAR(100),
date_joined DATE,
last_activity DATETIME
);

INSERT INTO users (id, email, date_joined, last_activity)
VALUES (1, "user1@domain.com", "2014-12-12", "2016-04-08 12:34:54");
INSERT INTO users (id, email, date_joined, last_activity)
VALUES (2, "user2@domain.com", "2014-12-12", "2017-02-13 11:46:53");
INSERT INTO users (id, email, date_joined, last_activity)
VALUES (3, "user3@domain.com", "2014-12-13", "2017-04-04 05:12:07");
```



**Задание №2**
create table users ( id int(10) unsigned, email varchar (100), date_joined date, last_activity datetime ); insert into users (id, email, date_joined,last_activity) values (1,'user1@domain.com', '2014-12-12','2016-04-08 12:34:54'), (2,'user2@domain.com', '2014-12-12','2017-02-13 11:46:53'), (3,'user3@domain.com', '2014-12-13','2017-04-04 05:12:07'); Создайте таблицу calendar для хранения календаря посетителей. В таблице должны быть следующие поля:

id – идентификатор записи в календаре, целое положительное; user_id – идентификатор пользователя, целое положительное; doctor_id – идентификатор доктора, целое положительное; visit_date – дата и время визита (точность до секунд).



![5379620308778087126](https://github.com/user-attachments/assets/4f861f6f-f29b-4e09-947d-7ac61f4d7107)



Неверное решение:

```
Create table calendar (
id int unsigned,
user_id int unsigned,
doctor_id int unsigned,
visit_date datetime);
Insert into calendar (id, user_id, doctor_id, visit_date)
Values (1, 1914 , 1, '2017-04-08 12:00:00'),
(2, 12, 1, '2017-04-08 12:30:00'),
(3, 4641, 2, '2017-04-09 09:00:00'),
(4, 4641, 2,'2017-04-09 09:00:00'),
(5, 15, 2,'2017-04-09 10:00:00')
```


Правильное решение:


```
Create table calendar (
id int unsigned,
user_id int unsigned,
doctor_id int unsigned,
visit_date datetime);
Insert into calendar (id, user_id, doctor_id, visit_date)
Values 
(1, 1914 , 1, '2017-04-08 12:00:00'),
(2, 12, 1, '2017-04-08 12:30:00'),
(3, 4641, 2, '2017-04-09 09:00:00'),
(4, 784, 1,'2017-04-08 13:00:00'),
(5, 15, 2,'2017-04-09 10:00:00')
```


**Задание №3**
Создайте таблицу users , в которой будут следующие поля:

id — идентификатор, целые положительные числа.

first_name— имя, строки до 50 символов.

last_name — фамилия, строки до 60 символов.

bio — биография, текст до 65000 символов.



![5379620308778087125](https://github.com/user-attachments/assets/ad078db5-963a-462f-95c0-c1d676168da0)


Неверное решение:


```
create table users (
id int (10) unsigned,
first_name varchar (50) unsigned,
last_name varchar (60) unsigned,
bio text
);
INSERT INTO users (id, first_name, last_name, bio)
VALUES
(1,'Антон','Кулик','С отличием окончил 39 лицей.'),
(2,'Сергей','Давыдов',''),
(3,'Дмитрий','Соколов','Профессиональный программист.')
```


Правильное решение:


```
create table users (
id int (10) unsigned,
first_name varchar (50),
last_name varchar (60),
bio text
);
INSERT INTO users (id, first_name, last_name, bio)
VALUES
(1,'Антон','Кулик','С отличием окончил 39 лицей.'),
(2,'Сергей','Давыдов',''),
(3,'Дмитрий','Соколов','Профессиональный программист.')
```
