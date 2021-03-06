# Примеры простых запросов SQL

Смоделирован фрагмент таблицы "БД книжного магазина". 	
				
#### 1. Создание таблицы: book_amital	

| ID | Наименование | Автор| цена | кол-во на складе |
|:---:|:----:|:----:|:----:|:----------|
| ID | Name | аuthor| price | quantity_stock |
| 1 | Легенды и сказки Востока | Дорошевич Влас | 786 | 6 |
| 2 | "Я вас любил..."| Пушкин А.С. | 885 | 4 |
| 3 | Старый Петербург. Рассказы о былой жизни столицы | Пыляев М.И. | 834 | 20 |
| 4 | Волшебник Изумрудного города: сказка | Волков А.М. | 814 | 15 |
| 5 | Тексты песен для детского сада. Раз-два-радугa|  | 12 | 5 |

#### Скрин из MySQL Workbench 8.0 CE

![Таблица: book_amital](https://github.com/TanyaGL11/---SQL/blob/main/%D0%9F%D1%80%D0%BE%D1%81%D1%82%D1%8B%D0%B5%20%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D1%8B1.png "BA")

### 2.Строка для добавления	

| ID | Наименование | Автор| цена | кол-во на складе |
|:---:|:----:|:----:|:----:|:----------|
| ID | Name | аuthor| price | quantity_stock |
| 1 | Сказка о мертвой царевне | Пушкин А.С. | 345 | 3 |

#### Описание запросов и реализованных задач

| Запросы | Задачи |
|:----|:---------|
| USE book | выбрать БД |
| SELECT * FROM book_amital | показать ВСЮ таблицу |
| INSERT INTO book_amital (`name`) VALUES ("Сказка о мертвой царевне") | создать новую строку, в столбец наименование записать - Сказка о мертвой царевне |
| UPDATE `book`.`book_amital` SET `autor` = 'Пушкин А.С.' WHERE (`id` = '7') | добавить данные в стр.7, автор - Пушкин А.С. |
| UPDATE `book`.`book_amital` SET `price` = 345  WHERE (`id` = '7') | добавить данные в стр.7, цена - 345 |
| UPDATE `book`.`book_amital` SET `quantity_stock` = 3  WHERE (`id` = '7') | добавить данные в стр.7, количество на складе -3 |

##### Скрин из MySQL Workbench 8.0 CE

![Таблица: book_amital](https://github.com/TanyaGL11/---SQL/blob/main/%D0%9F%D1%80%D0%BE%D1%81%D1%82%D1%8B%D0%B5%20%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D1%8B%20%D1%81%20%D0%B4%D0%BE%D0%B1%20%D1%81%D1%82%D1%80%D0%BE%D0%BA%D0%B81.png "BA")

### 3. Выборка(**WHERE**)

| Запросы | Задачи |
|:----|:---------|
| SELECT * FROM book_amital WHERE autor LIKE '%Пушкин%' | показать строки таблицы товара, автор - "Пушкин" |

##### Скрин из MySQL Workbench 8.0 CE

![Таблица: book_amital](https://github.com/TanyaGL11/---SQL/blob/main/%D0%9A%D0%BD%D0%B8%D0%B3%D0%B8%20%D0%9F%D1%83%D1%88%D0%BA%D0%B8%D0%BD%D0%B01.png "BA")

### 4. Выборка c ограничениями(**WHERE, ORDER BY**)

| Запросы | Задачи |
|:----|:---------|
| SELECT * FROM book_amital WHERE quantity_stock is NOT null ORDER BY autor,quantity_stock,price DESC | показать строки таблицы товара, который есть на складе, по порядку "от А до Я" - авторов и по убыванию цен |

##### Скрин из MySQL Workbench 8.0 CE

![Таблица: book_amital](https://github.com/TanyaGL11/---SQL/blob/main/%D0%92%D1%8B%D0%B1%D0%BE%D1%80%D0%BA%D0%B01.png "BA")

### 5. Удаление строки.

| Запросы | Задачи |
|:----|:---------|
| DELETE FROM  book_amital WHERE id>5 | удалить строку с ID>5 |

### 6. Выборка с лимитом.

| Запросы | Задачи |
|:----|:---------|
| SELECT * FROM book_amital WHERE autor LIKE '%Пушкин%' LIMIT 1 | вывести первую книгу Пушкина |

##### Скрин из MySQL Workbench 8.0 CE

![Таблица: book_amital](https://github.com/TanyaGL11/---SQL/blob/main/%D0%92%D1%8B%D0%B1%D0%BE%D1%80%D0%BA%D0%B0%20%D0%BF%D0%BE%20%D0%BB%D0%B8%D0%BC%D0%B8%D1%82%D1%83.png "BA")

Запросы можно здесь [скачать](https://github.com/TanyaGL11/---SQL/blob/main/%D0%9F%D1%80%D0%B8%D0%BC%D0%B5%D1%80%D1%8B%20%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D0%BE%D0%B2.sql)
