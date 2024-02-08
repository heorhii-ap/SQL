# SQL запросы

Здесь представлены примеры SQL запросов в работе с БД.

[База данных "Библиотека"](#library)

## База данных "Библиотека" <a name="library"></a>

### Описание БД

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

![1_select](https://github.com/heorhii-ap/SQL/assets/143074323/3849e69b-6b22-4098-96e8-007ec1cd8c48)

</details><br>

 Выбрать все столбцы из таблицы ```authors```
 ```
SELECT 
    * 
FROM 
    authors;
```

<details><summary>Результат запроса</summary><br>  

![2_select](https://github.com/heorhii-ap/SQL/assets/143074323/653b5878-82da-406d-97b7-146e530050c4)

</details><br>

 Выбрать все столбцы из таблицы ```genre```
 ```
SELECT 
    * 
FROM 
    genre;
```

<details><summary>Результат запроса</summary><br> 

![3_select](https://github.com/heorhii-ap/SQL/assets/143074323/06aecbdd-66a4-4d9d-b31e-29e8f9d89fe0)

</details><br>

### Срезы данных WHERE

 Выбрать все книги Достоевского (author_id = 9)

```
SELECT
    title
FROM
    books
WHERE
    author_id = 9;
```

<details><summary>Результат запроса</summary><br> 

![4_where](https://github.com/heorhii-ap/SQL/assets/143074323/aa8c62c4-9f82-4fc6-a7de-f21536802fe0)

</details><br>

Все книги, которые написал не Достоевский (author_id = 9)

```
SELECT
    title
FROM
    books
WHERE
    author_id != 9;
```

<details><summary>Результат запроса</summary><br> 

![5_where](https://github.com/heorhii-ap/SQL/assets/143074323/a1cbb4b7-2936-4ecc-8682-62c9330f4d8c)

</details><br>

Все книги дороже 200

```
SELECT
    title,
    price
FROM
    books
WHERE
    price > 200;
```

<details><summary>Результат запроса</summary><br> 

![6_where](https://github.com/heorhii-ap/SQL/assets/143074323/f3668f71-d53e-405b-bfc9-2f4d03e761a6)

</details><br>


