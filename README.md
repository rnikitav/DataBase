# DataBase


### Урок 1
Дорогие студенты!

К этому уроку очень простое, но важное для построения дальнейших уроков дополнительное задание.

Напишите ответы на вопросы в комментарий при сдаче практического задания:
1) Какие у вас ожидания от курса? Есть ли конкретные вопросы по теме Базы данных?
2) В какой сфере работаете сейчас?
3) Если в IT, то какой у вас опыт (инструменты, технологии, языки программирования)?


### Урок 2

1) Установите СУБД MySQL. Создайте в домашней директории файл .my.cnf, задав в нем логин и пароль, который указывался при установке.
2) Создайте базу данных example, разместите в ней таблицу users, состоящую из двух столбцов, числового id и строкового name.
3) Создайте дамп базы данных example из предыдущего задания, разверните содержимое дампа в новую базу данных sample.
4) (по желанию) Ознакомьтесь более подробно с документацией утилиты mysqldump. Создайте дамп единственной таблицы help_keyword базы данных mysql. Причем добейтесь того, чтобы дамп содержал только первые 100 строк таблицы.


### Урок 3. Вебинар. Введение в проектирование БД

1) Написать крипт, добавляющий в БД vk, которую создали на занятии, 3 новые таблицы (с перечнем полей, указанием индексов и внешних ключей)

### Урок 4. Вебинар. CRUD-операции

1) Заполнить все таблицы БД vk данными (по 10-100 записей в каждой таблице)
2) Написать скрипт, возвращающий список имен (только firstname) пользователей без повторений в алфавитном порядке
3) Написать скрипт, отмечающий несовершеннолетних пользователей как неактивных (поле is_active = false). Предварительно добавить такое поле в таблицу profiles со значением по умолчанию = true (или 1)
4) Написать скрипт, удаляющий сообщения «из будущего» (дата больше сегодняшней)
5) Написать название темы курсового проекта (в комментарии)


### Урок 5. Видеоурок. Операторы, фильтрация, сортировка и ограничение. Агрегация данных

1) Пусть в таблице users поля created_at и updated_at оказались незаполненными. Заполните их текущими датой и временем.
2) Таблица users была неудачно спроектирована. Записи created_at и updated_at были заданы типом VARCHAR и в них долгое время помещались значения в формате "20.10.2017 8:10". Необходимо преобразовать поля к типу DATETIME, сохранив введеные ранее значения.
3) В таблице складских запасов storehouses_products в поле value могут встречаться самые разные цифры: 0, если товар закончился и выше нуля, если на складе имеются запасы. Необходимо отсортировать записи таким образом, чтобы они выводились в порядке увеличения значения value. Однако, нулевые запасы должны выводиться в конце, после всех записей.
4) (по желанию) Из таблицы users необходимо извлечь пользователей, родившихся в августе и мае. Месяцы заданы в виде списка английских названий ('may', 'august')
5) (по желанию) Из таблицы catalogs извлекаются записи при помощи запроса. SELECT * FROM catalogs WHERE id IN (5, 1, 2); Отсортируйте записи в порядке, заданном в списке IN.

- Агрегация данных 
1) Подсчитайте средний возраст пользователей в таблице users
2) Подсчитайте количество дней рождения, которые приходятся на каждый из дней недели. Следует учесть, что необходимы дни недели текущего года, а не года рождения.
3) (по желанию) Подсчитайте произведение чисел в столбце таблицы



### Урок 6. Вебинар. Операторы, фильтрация, сортировка и ограничение. Агрегация данных

1) Пусть задан некоторый пользователь. Из всех пользователей соц. сети найдите человека, который больше всех общался с выбранным пользователем (написал ему сообщений).
2) Подсчитать общее количество лайков, которые получили пользователи младше 10 лет.
3) Определить кто больше поставил лайков (всего): мужчины или женщины.


### Урок 7. Видеоурок. Сложные запросы

1) Составьте список пользователей users, которые осуществили хотя бы один заказ orders в интернет магазине.
2) Выведите список товаров products и разделов catalogs, который соответствует товару.
3) (по желанию) Пусть имеется таблица рейсов flights (id, from, to) и таблица городов cities (label, name). Поля from, to и label содержат английские названия городов, поле name — русское. Выведите список рейсов flights с русскими названиями городов.


### Урок 9. Видеоурок. Транзакции, переменные, представления. Администрирование. Хранимые процедуры и функции, триггеры

1.Практическое задание по теме “Транзакции, переменные, представления”

* В базе данных shop и sample присутствуют одни и те же таблицы, учебной базы данных. Переместите запись id = 1 из таблицы shop.users в таблицу sample.users. Используйте транзакции.

* Создайте представление, которое выводит название name товарной позиции из таблицы products и соответствующее название каталога name из таблицы catalogs.

2.Практическое задание по теме “Администрирование MySQL” (эта тема изучается по вашему желанию)

* Создайте двух пользователей которые имеют доступ к базе данных shop. Первому пользователю shop_read должны быть доступны только запросы на чтение данных, второму пользователю shop — любые операции в пределах базы данных shop.

* (по желанию) Пусть имеется таблица accounts содержащая три столбца id, name, password, содержащие первичный ключ, имя пользователя и его пароль. Создайте представление username таблицы accounts, предоставляющий доступ к столбца id и name. Создайте пользователя user_read, который бы не имел доступа к таблице accounts, однако, мог бы извлекать записи из представления username.

3.Практическое задание по теме “Хранимые процедуры и функции, триггеры"

* Создайте хранимую функцию hello(), которая будет возвращать приветствие, в зависимости от текущего времени суток. С 6:00 до 12:00 функция должна возвращать фразу "Доброе утро", с 12:00 до 18:00 функция должна возвращать фразу "Добрый день", с 18:00 до 00:00 — "Добрый вечер", с 00:00 до 6:00 — "Доброй ночи".

* В таблице products есть два текстовых поля: name с названием товара и description с его описанием. Допустимо присутствие обоих полей или одно из них. Ситуация, когда оба поля принимают неопределенное значение NULL неприемлема. Используя триггеры, добейтесь того, чтобы одно из этих полей или оба поля были заполнены. При попытке присвоить полям NULL-значение необходимо отменить операцию.

* (по желанию) Напишите хранимую функцию для вычисления произвольного числа Фибоначчи. Числами Фибоначчи называется последовательность в которой число равно сумме двух предыдущих чисел. Вызов функции FIBONACCI(10) должен возвращать число 55.


### Урок 11. Видеоурок. Оптимизация запросов. NoSQL

1) Создайте таблицу logs типа Archive. Пусть при каждом создании записи в таблицах users, catalogs и products в таблицу logs помещается время и дата создания записи, название таблицы, идентификатор первичного ключа и содержимое поля name.
2) (по желанию) Создайте SQL-запрос, который помещает в таблицу users миллион записей.

### Урок 13.  Курсовой проект
* Создание БД для интернет магазина одежды
