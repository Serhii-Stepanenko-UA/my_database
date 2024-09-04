--Створення бази даних SQLite БД через DB BROWSER FOR SQLITE
    --(DB4S)з назвою my_database

--Створення таблиці з назвою users в базі даних my_database,
	--яка буде містити наступні поля:
	--id (цілочисельний тип, автоінкрементний, первинний ключ),
	--name (рядковий тип),
	--age (цілочисельний тип),
	--email (рядковий тип).

CREATE TABLE IF NOT EXISTS users (
  id INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT,
  name TEXT NOT NULL,
  age INTEGER,
  email TEXT
);

--Вставка данних в таблицю users - три записи:
INSERT INTO users
(name, age, email)
VALUES
('John', 30, 'john@example.com'),
('Alice', 25,'alice@example.com'),
('Bob', 35, 'bob@example.com');

--Вибірка данних - усіх записів з таблиці users.
SELECT * FROM users;

--Видалення даних - запис користувача з ім'ям"Bob" з таблиці users.
DELETE FROM users WHERE name = 'Bob';

--Перевірка, що користувач з ім'ям "Bob" був успішно видалений.
SELECT * FROM users;