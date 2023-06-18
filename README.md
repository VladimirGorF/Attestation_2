# Attestation_2

Задание
1. Используя команду cat в терминале операционной системы Linux, создать два файла Домашние животные (заполнив файл собаками, кошками, хомяками) и Вьючные животными заполнив файл Лошадьми, верблюдами и ослы), а затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя (Друзья человека).
2. Создать директорию, переместить файл туда.
3. Подключить дополнительный репозиторий MySQL. Установить любой пакет из этого репозитория.
4. Установить и удалить deb-пакет с помощью dpkg. 5. Выложить историю команд в терминале ubuntu

mysql
mysql> show databases;
mysql> CREATE DATABASE IF NOT EXISTS Homofriends; mysql> use Homofriends;
mysql> CREATE TABLE IF NOT EXISTS animals( ID INT PRIMARY KEY AUTO_INCREMENT, name Varchar(20) NOT NULL, weight INT NOT NULL, height INT NOT NULL, age INT NOT NULL);
mysql> CREATE TABLE IF NOT EXISTS homeanimals (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(20) NOT NULL, command VARCHAR(20) NOT NULL, age INT NOT NULL);
mysql> CREATE TABLE IF NOT EXISTS packanimals (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(20) NOT NULL, command VARCHAR(20) NOT NULL, age INT NOT NULL);
mysql> INSERT homeanimals (name, command, age) VALUES ("dog", "run", 2), ("cat","jump", 3),
("humster", "lie", 1);
mysql> INSERT packanimals (name, command, age) VALUES ("horse", "run", 2), ("camel","stay",
3), ("donkey", "cry", 2);
mysql> DELETE FROM packanimals -> WHERE name = "camel";
mysql> CREATE TABLE IF NOT EXISTS horses (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(20) NOT NULL, command VARCHAR(20) NOT NULL, age INT NOT NULL);
mysql> CREATE TABLE IF NOT EXISTS donkeys (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(2
0) NOT NULL, command VARCHAR(20) NOT NULL, age INT NOT NULL);
mysql> INSERT horses (name, command, age) VALUES ("Nura", "run", 2), ("Pona","stay", 3), ("Zorka", "cry", 2);
mysql> INSERT donkeys (name, command, age) VALUES ("Sura", "run", 2), ("Topa","stay", 3), ("Chuka", "cry", 2);
mysql> SELECT * FROM horses -> UNION ALL
-> SELECT * FROM donkeys;
mysql> CREATE TABLE horseanddonkey AS -> SELECT * FROM horses

-> UNION ALL
-> SELECT * FROM donkeys;
mysql> CREATE TABLE yangAnimals AS -> SELECT * FROM horseanddonkey -> WHERE age = 2;
mysql> SELECT COUNT(age) FROM yangAnimals;
mysql> CREATE TABLE newOneTable AS
-> SELECT * FROM homeanimals UNION ALL SELECT * FROM
yangAnimals UNION ALL
-> SELECT * FROM horseanddonkey -> UNION ALL
-> SELECT * FROM packanimals
-> UNION ALL
-> SELECT * FROM horses
-> UNION ALL
-> SELECT * FROM donkeys;
mysql> select * from newOneTable; mysql> exit


   
