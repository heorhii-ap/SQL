# SQL запросы

Здесь представлены примеры SQL запросов в работе с БД.

[База данных "Библиотека"](#library)

## База данных "Библиотека" <a name="library"></a>

### Описание базы данных

База данных состоит из трех таблиц ```books```, ```authors``` и ```genre```.

ER-диаграмма таблиц выглядит так:

<p align="left">
  <img width="400" src="https://github.com/heorhii-ap/SQL/assets/143074323/5bff18cf-143e-489d-863e-c4b63bf97eeb">
</p>

<details>
<summary>Таблица books — информация о книгах.</summary><br> 

Поля:

* ```id``` - поле с уникальным идентификатором. Тип данных: ```integer```. Первичный ключ.

* ```title``` - название книги. Тип данных: ```varchar```.
* ```genre``` - жанр книги.  Тип данных: ```integer```. Внешний ключ.
* ```author_id``` - автор книги. Тип данных: ```integer```. Внешний ключ.
* ```date_pub``` - дата публикации. Тип данных: ```timestamp```.
* ```page``` - количество страниц. Тип данных: ```integer```.
* ```price``` - цена книги. Тип данных: ```integer```.
* ```rating``` - рейтинг книги. Тип данных: ```float```.

</details>

<details>
<summary>Таблица authors — информация об авторах книг.</summary><br> 

Поля:

* ```id``` - поле с уникальным идентификатором. Тип данных: ```integer```. Первичный ключ.
* ```first_name``` - имя автора. Тип данных: ```varchar```.
* ```last_name``` - фамилия автора. Тип данных: ```varchar```.

</details>

<details>
<summary>Таблица genre — информация о жанре книг.</summary><br> 

Поля:

* ```id``` - поле с уникальным идентификатором. Тип данных: ```integer```. Первичный ключ.
* ```name``` - название жанра. Тип данных: ```varchar```.

</details>

<details>
<summary>Таблица books — информация о книгах.</summary><br> 

</details>

### Оператор SELECT

Выбрать все столбцы из таблицы ```books```
```
SELECT 
    * 
FROM 
    books;
```

<details><summary>Результат запроса</summary><br> 

</details><br>

 Выбрать все столбцы из таблицы ```authors```
 ```
SELECT 
    * 
FROM 
    authors;
```

<details><summary>Результат запроса</summary><br>  

</details><br>

 Выбрать все столбцы из таблицы ```genre```
 ```
SELECT 
    * 
FROM 
    genre;
```

<details><summary>Результат запроса</summary><br> 

</details><br>
