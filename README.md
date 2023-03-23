# Разработка Интернет Приложений (РИП) 2022

Отчеты по лабораторным работам и ДЗ отправлять на почту `aikanev@bmstu.ru`

## [Видеозаписи лекций в youtube](https://youtube.com/playlist?list=PLLELLTvDgUQ9cpB1XzSuZ0mNSBkbjVNJ_)
#### Образ виртуальной машины Linux [Ubuntu 20.04](https://github.com/iu5git/Standards/blob/main/Linux/Linux.md) для выполнения заданий курса 

## Лекции
### Бекенд
[Лекция 1. История Web, трехуровневая модель приложений, MVC](https://github.com/iu5git/web-2022/blob/main/lectures/web_intro.pdf) 

[Лекция 2. Методология Agile, состав команды. Диаграммы UML](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_2_Agile_UML.pdf)

[Лекция 3. Основы Web, шаблонизация, Django](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_3_Web_Django.pdf)

[Лекция 4. Базы данных, ER, PostgreSQL. ORM. Админка Django. Курсоры](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_4_Databases_Django_ORM.pdf)

[Лекция 5. Веб-сервис. Swagger. Микросервисы](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_5_Web_Service.pdf)

[Лекция 6. Работа в git. Примеры специализированных сервисов - S3, уведомления, очереди](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_6_Special_Services.pdf)

### Фронтенд
[Лекция 7. Введение в фронтенд и React](https://github.com/iu5git/web-2022/blob/main/lectures/Lecture_7_React_Introduction.pdf)

[Лекция 8. React, сборка, компоненты](/lectures/Lecture_8_React.pdf)

[Лекция 9. Redux, hooks](/lectures/Lecture_9_Redux.pdf)

[Лекция 10. Ajax, запросы на React. WebSocket](/lectures/Lecture_10_Ajax.pdf)

[Лекция 11. Авторизация, куки, хранилище сессий](/lectures/Lecture_11_Authorization.pdf) 

[Лекция 12. JWT. SSO](/lectures/Lecture_12_jwt.pdf) 

### Мобильные приложения

[Лекция 13. Общая лекция про мобильные приложения. PWA](/lectures/Lecture_13_PWA.pdf) 

[Лекция 14. Плюсы и минусы React Native. Сетевое взаимодействие на Swift](/lectures/Lecture_14_Swift.pdf) 

### Инфраструктура

[Лекция 15. Резюме, Tauri, Agile, DevOps](/lectures/Lecture_15_Deploy.pdf)

## Лабораторные работы
У каждого своя предметная область на весь курс: бронирование отелей, билетов в театр/кинотеатр, онлайн-магазин

Основной вариант лаб по беку - это Django. Но есть ещё варианты на `Go`, `Java`, `C#` и `Node.js`

При защите необходимо продемонстрировать работу приложения, UML диаграмму, репозиторий github с кодом и ответить на вопросы.

[Инструкция по работе c Python](/tutorials/python/python.md)

#### Лабораторная работа №1
Базовая шаблонизация в Django для словаря. Создание базового интерфейса для просмотра списка (отели, товары, рейсы и тд) с ссылками и частью полей (цена, город) и при переходе по ссылке другая страница с более подробной информацией о товаре (описание, картинка и тд). 

В приложении должны быть использованы стили, для каждого элемента списка подгружается свое изображение. 

Добавить поле input для ограничения количества записей, отображаемых на странице (по умолчанию отображать все).

На выбор `Django`, `Go`, `Spring`, `Node.js`

- **Порядок показа**: показать две страницы приложения, объяснить шаблоны, контроллеры этих страниц и коллекцию данных
- **Контрольные вопросы**: MVC, Django, шаблонизация, HTTP, Web, HTML

* [Методические указания Django](/tutorials/lab1-py/lab1_tutorial.md)
* [Методические указания Golang](/tutorials/lab1-go/README.md)

#### Лабораторная работа №2
Создание **базы данных** `PostgreSQL`/`MySQL` (`SQLite` использовать нельзя), подключение к шаблонизатору. Создание **админки**.

Для карточек таблицы услуг добавить кнопку удаления услуги с помощью выполнения SQL запроса.

**Обязательные таблицы**: таблица услуг/товаров - словарь, таблица фактов - например бронирования (с датами и статусом, три даты и менеджер), таблица пользователей

Статусы: введен, в работе, завершён, удалён

**ER диаграмма**: таблицы, связи, столбцы, типы столбцов и их длина, первичные, вторичные ключи

- **Порядок показа**: показать панель администратора, добавить запись, посмотреть данные через select в БД, показать шаблоны страниц. Пояснить модели, контроллеры для созданных таблиц
- **Контрольные вопросы**: ORM, SQL, модель и миграции

* [Методические указания Django](/tutorials/lab2-py/lab2_tutorial.md)
* [Методические указания Golang](/tutorials/lab2-go/README.md)

#### Лабораторная работа №3
Создание **веб-сервиса** для получения/редактирования данных из вашей БД. Требуется разработать методы для основных (минимум трех) таблиц вашего приложения. Проверка в insomnia/swagger/postman. 

Добавить метод для подсчета суммы (количества) покупок/бронирований за определенную дату через обращение к методам модели.

**Диаграмма компонентов+классов**: компонент сервиса, интерфейс, структура модели по классам

- **Порядок показа**: выполнить GET списка, сделать POST новой записи, показать новые данные через select. Объяснить модели, сериализаторы, контроллеры, роутеры для методов веб-сервиса
- **Контрольные вопросы**: веб-сервис, микросервисы, REST, RPC

* [Методические указания DRF](/tutorials/lab3-py/lab3_tutorial.md)
* [Методические указания Golang](/tutorials/lab3-go/README.md)

#### Лабораторная работа №4
Базовая работа по фронтенду. Карточки элементов, навигация. Необходимо разработать страницы, аналогичные лабораторной работе №1 для просмотра услуг. Использовать компоненты `React-Bootstrap`. Карточки наполняются через mock-объекты.

Подключение разработанного интерфейса фронтенда к веб-сервису из лабораторной №3. Ajax-запросы написать самостоятельно через fetch.

Навигация по двум страницам должна быть организована посредством **Навигационной цепочки** `Breadcrumbs`: [Магазин](/README.md) / [Название услуги](/README.md)

На выбор `React`, `Vue`, `Angular`

**Deployment диаграмма**: узлы фронтенда, веб-сервиса, базы данных, web-сервера со статикой

- **Порядок показа**: показать две страницы приложения в браузере. Объяснить код страниц, показать коллекцию данных
- **Контрольные вопросы**: react, props, компонент, элемент, состояние, хуки, жизненный цикл компонента

* [Методические указания](/tutorials/lab4/lab4_tutorial.md)

#### Лабораторная работа №5

Добавление **главного меню** приложения. Развертывание React приложения в `GitHub Pages` (+1 балл).

Добавление кнопки бронирования на странице услуг. Добавление **станицы корзины**, в корзине добавить кнопку удаления.

Добавление **менеджера состояний** `redux` для кеширования полученных по API данных товаров/услуг и их использования в компонентах, а также для хранения состояния корзины (пока без самих POST запросов)

В приложении должно быть реализовано переключение между интерфейсом гостя и интерфейсом пользователя, кнопки `Вход`/`Выход`- без аутентификации, просто смена состояния. При выходе должно сбрасываться состояние корзины.

**Sequence диаграмма**: получение `HTML` страницы, `AJAX` запросы

- **Порядок показа**: показать страницы вместе с запросами в браузере на вкладке Network. Пояснить использование `redux` в приложении: store, reducers и тд 
- **Контрольные вопросы**: AJAX, json, XmlHttpRequest/fetch, redux, контекст

* [Методические указания](/tutorials/lab5/lab5_tutorial.md)

#### Лабораторная работа №6
Добавление страницы просмотра для таблицы бронирований/заказов клиента, подключить к web-сервису.

Для подключения к нужным сервисам/методам бэкенда использовать автоматическую кодогенерацию через swagger (+2 балла). На бэкенде должна быть доступна админская панель.

Добавление фильтрации и поиска на странице услуг (сама фильтрация на стороне бэкенда):
1. По наименованию услуги или дате начала
2. По диапазону значений (цене, количеству, размеру). Максимальное и минимальное значение запрашиваются с сервера

**Activity диаграмма** для итогового бизнес-процесса из ДЗ: описание бизнес-процесса, разделение на дорожки по ролям пользователей, действия соответствуют операциям пользователей в вашей системе.

- **Порядок показа**: показать фильтрацию и добавление заказа. Пояснить реализацию фильтрации в бэкенде и реализацию на фронтенде взаимодействия с сервисом  
- **Контрольные вопросы**: AJAX, json, XmlHttpRequest/fetch, react, props, компонент, элемент, состояние, веб-сервис, микросервисы, REST, RPC

* [Методические указания](/tutorials/lab6/lab6_tutorial.md)

#### Лабораторная работа №7
Добавить модель таблицы пользователей, реализовать методы бэкенда и окна фронтенда для **аутентификации** и **регистрации**. Авторизация через хранение сессий (`Redis` - дополнительные баллы) и куки. Автозаполнение пользователя в таблице фактов при создании нового бронирования.

Добавить ограничение на вызовы методов веб-сервиса для клиента. Без авторизации в Insomnia/Swagger должно быть доступно только чтение-получение данных через API, с авторизацией доступны другие методы.

**Диаграмма компонентов/классов** с детализацией бэкенда: все компоненты системы с интерфейсами, выделить сервисы и интерфейсы данных и авторизации

- **Порядок показа**: показать авторизацию в браузере и содержимое localStorage/cookie. Использовать его для запроса через insomnia
- **Контрольные вопросы**: куки, сессия, redis, jwt, авторизация, аутентификация

* [Настройка через WSL](https://github.com/iu5git/Networking/tree/main/kafka_wsl)
* [Методические указания DRF Redis](https://github.com/iu5git/web-2022/blob/main/tutorials/lab7-py/lab7_tutorial.md)
* [Методические указания Golang JWT](https://github.com/iu5git/web-2022/tree/main/tutorials/lab7-go/README.md)

#### Лабораторная работа №8
Создание мобильного нативного приложения (дополнительные баллы) или `PWA` с адаптивной версткой для телефона. 

Требуется реализовать подключение к web-сервису. Просмотр услуг (товаров и тд), без бронирования и редактирования. 

- **Порядок показа**: показать адаптивный интерфейс в браузере через **отзывчивое устройство**, объяснить реализацию адаптивности.
- **Контрольные вопросы**: PWA, service worker, manifest.json, media queries

* [iOS (Swift)](https://github.com/iu5git/web-2022/blob/main/tutorials/ios_tutorial/ios_tutorial.md)
* [Android (Java)](https://github.com/iu5git/web-2022/blob/main/tutorials/android_tutorial/android_tutorial.md)
* [React Native + Redux Toolkit](/tutorials/react-native/react_native.md)
* [Progressive Web App](/tutorials/pwa/PWA.md)

## Домашнее задание
Добавление роли пользователя-менеджера контента, доработка под эту роль фронтенда и веб-сервиса:
1. **Редактирование таблицы услуг**: добавление, редактирование, удаление
2. **Изменение статусов таблицы бронирования**: последовательная смена статусов вперед или назад; недоступно изменение статуса с любого на любой; при изменении статуса должно происходить изменение других полей таблицы (обязательно дата оплаты, дата завершения заказа; дополнительно назначение платежа, адрес доставки и тд)
3. **Фильтрация записей таблицы бронирования по дате и статусу**. Список статусов начитывается с сервера через метод API

Доработка ролевой модели - ограничение прав на интерфейс для пользователь-клиента. Добавление главного меню приложения.

Добавить ограничение на вызовы методов веб-сервиса для клиента и отдельно для менеджера. Без авторизации в Insomnia/Swagger должно быть доступно только чтение-получение данных через API 

- **Порядок показа**: показать рабочее место пользователя и менеджера. Объяснить разделение прав для разных ролей на бэкенде
- **Контрольные вопросы**: куки, сессия, AJAX, json, веб-сервис

* [Методические указания и примеры диаграмм](/tutorials/homework)

#### Оформление единого отчёта 
Добавить диаграмму состояний для бронирований или услуг и диаграмму прецедентов. 

Актуализировать все диаграммы из лабораторных, добавить краткое описание к диаграммам. Все диаграммы должны соответствовать реализованной вами системе. Объем не меньше 1000 слов.

Шесть разделов отчета: 
1. **Техническое задание**: цель, задачи, требования к функциональным характеристикам (какие есть пользователи и какие у них возможности), требования к программному обеспечению (какое ПО должно быть на клиенте и на сервере для работы вашей системы)
2. **Введение** (описание предметной области, актуальность)
3. **Бизнес-процесс**. Диаграмма прецедентов, диаграмма состояний и деятельности
4. **Архитектура**. Диаграммы развертывания, ER с назначением таблиц и диаграмма компонентов (классов) с детализацией бэкенда и фронтенда
5. **Алгоритмы**. Диаграмма последовательности
6. **Описание интерфейса**. Перечень окон и их назначение

## Вопросы к экзамену
1. Опишите шаблон MVC, структуру и назначение компонентов.
2. Опишите схему, как реализован шаблон MVC в фреймворке Django.
3. Что такое Django? Его назначение и возможности.
4. Что такое шаблонизация Django? Приведите примеры.
5. Опишите протокол HTTP. Схему работы и основные понятия.
6. Опишите стек протоколов интернета TCP/IP.
7. Перечислите основные составляющие web и опишите их.
8. Что такое HTML, CSS? Приведите примеры.
9. Что такое URI? Опишите элементы URI для HTTP.
10. Виды баз данных. Приведите примеры и отличия.
11. Объясните назначение ORM, ее составляющие. Укажите преимущества и недостатки ORM.
12. Что такое модель и миграция?
13. Укажите группы SQL запросов, их примеры и назначение.
14. Что такое веб-сервис? Отличие от веб-сервера.
15. Что такое Web API? Назначение и применение.
16. Микросервисная архитектура. Отличия от монолитной архитектуры.
17. Перечислите требования REST, опишите их.
18. Что такое RPC? Варианты RPC и их отличия.
19. Что такое Swagger? Назначение и использование.
20. Что такое AJAX? Схема работы и назначение.
21. Назначение JSON и XML. Примеры и отличия.
22. Что такое git? Опишите схему работы с ветками GitHub.
1. Методология разработки Agile. Состав IT команды.
2. Перечислите основные диаграммы UML и их назначение.
3. Что такое Web реального времени? Что такое WebSocket?
4. Укажите отличия XmlHttpRequest и fetch. Приведите примеры.
5. Перечислите отличия Axios от fetch. Приведите примеры.
6. Что такое React? Что такое компонент, его состояния и свойства.
7. Структура React проекта. Назначение Babel и WebPack.
8. Жизненный цикл React компонента.
9. Назначение хуков useState и useEffect.
10. Назначение хуков useContext и useReducer.
11. Опишите схему работы менеджера состояний Redux.
12. Опишите работу Redux на диаграмме последовательности.
13. Какие параметры передаются при создании Store? Их назначение.
14. Что такое Cors? Укажите варианты решения.
15. Что такое Redis? Его назначение и варианты применения.
16. Опишите схему авторизации с помощью JWT.
17. Опишите схему авторизации с помощью сессий.
18. Что такое авторизация и аутентификация? Укажите варианты авторизации и их отличия.
19. Что такое SSO? Схема работы.
20. Протокол OAuth. Схема работы.
21. Отличия мобильных и веб-приложения. Языки и технологии для разработки мобильных приложений.
22. Что такое pwa? Отличия от других вариантов приложений.
23. Плюсы и минусы разработки на React Native.
24. Назначение фреймворков Electron и Tauri. Их отличия.
25. Опишите этапы подхода DevOps. Назначение GitHub Pages.

#### Команда курса выражает благодарность за помощь в подготовке материалов для данного курса
1. Торжков Максим Сергеевич
2. Болдин Дмитрий Алексеевич
3. Петренко Сергей Сергеевич
4. Курганова Александра Геннадьевна
5. Федорова Антонина Алексеевна
6. Низовцев Роман Александрович
7. Коновалов Максим Владиславович
8. Толпаров Натан Русланович
9. Данилов Даниил Сергеевич
10. Балабанов Алексей Олегович
11. Ткаченко Владислав Львович
12. Ким Алексей Максимович