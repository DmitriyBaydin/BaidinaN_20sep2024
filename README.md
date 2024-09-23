# Вариант 1 - «Полезные продукты»

## Шаг 1. Base

### 

- Составлен чек-лист проверок для функциональности поиска на платформе https://altaivita.ru/ в Excel
- Составлен список вопросов к требованиям

### Уточнения от продакта:

- Данная функциональность очень важна для руководства. И в ближайшее время они хотят самостоятельно проверить ее работоспособность.
- Один из руководителей работает только в браузере FireFox developer-версии и любит размещать на половину экрана Телеграм, а на половину — браузер.
- Два других имеют в доступе только планшеты iPad Pro 12.9 (2022).
- Большинство пользователей, которые работают с этой функциональностью, используют Google Chrome.

## Шаг 2. API

### 
Составлена коллекция Postman, которая может провести смоук-тест корзины https://altaivita.ru/, и инструкцию по работе с ней.

Коллекция включает в себя:

- добавление товара
- изменение количества товара (увеличение)
- удаление товара.
Инструкция в файле с расширением .doc. с информацией о том, как работать с коллекцией, какие запросы включены, какие переменные и скрипты используются, что необходимо для авторизации.

## Шаг 3. SQL

### Дано описание БД «Полезные продукты»

Table 1. Products («Продукты»)
Columns:

- product_id (int, primary key)
- product_name (varchar)
- category_id (int, foreign key referencing Categories)
- calories (int)
- price (decimal)

Table 2. Categories («Категории»)
Columns:

- category_id (int, primary key)
- category_name (varchar)

Table 3. Nutritional Information («Пищевая ценность»)
Columns:

- product_id (int, foreign key referencing Products)
- protein (decimal)
- carbohydrates (decimal)
- fat (decimal)
- fiber (decimal)

### Связи таблиц

- Продукты и категории имеют отношение «один ко многим», причем продукты связаны с категориями через внешний ключ Category_id.
- Информация о пищевой ценности имеет однозначное отношение к продуктам, связываясь с продуктами через внешний ключ Product_id.

### Составлены запросы

- Все уникальные названия продуктов.
- Выведены id, название и стоимость продуктов с содержанием клетчатки (fiber) более 5 граммов.
- Выведены названия продукта с самым высоким содержанием белка (protein).
- Подсчитана общая сумма калорий для продуктов каждой категории, но не учитывайте продукты с нулевым жиром (fat = 0). Выведены id категории, сумма калорий.
- Рассчитана средняя цена товаров каждой категории. Выведины название категории, средняя цена.

Внимание!
Данные продуманы на основе описания и заполнены таблицы.
Скрипты по созданию и наполнению таблиц не представлены.

## Шаг 4. Auto

API и UI-тесты функциональности корзины интернет-магазина https://altaivita.ru/.

Используется:

- Python
- Selenium
- Requests
- pytest
- Allure

## Шаг 5. Soft

Работа, выполненная в четырех предыдущих шагах.
Показано выполнение запросов и интерфейс приложения.
