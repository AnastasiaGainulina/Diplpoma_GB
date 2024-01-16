Дипломная работа к профессии Python-разработчик «API Сервис заказа товаров для розничных сетей».
Описание
Приложение предназначено для автоматизации закупок в розничной сети через REST API.

Внимание! Все взаимодействие с приложением ведется через API запросы. Реализация фронтенд-приложения возможна только по желанию обучающегося

Пользователи сервиса:

Клиент (покупатель):

Делает ежедневные закупки по каталогу, в котором представлены товары от нескольких поставщиков.
В одном заказе можно указать товары от разных поставщиков.
Пользователь может авторизироваться, регистрироваться и восстанавливать пароль через API.
Поставщик:

Через API информирует сервис об обновлении прайса.
Может включать и отключать прием заказов.
Может получать список оформленных заказов (с товарами из его прайса).
Задача
Необходимо разработать backend-часть сервиса заказа товаров для розничных сетей на Django Rest Framework.

Базовая часть:

Разработка сервиса под готовую спецификацию (API);
Возможность добавления настраиваемых полей (характеристик) товаров;
Импорт товаров;
Отправка накладной на email администратора (для исполнения заказа);
Отправка заказа на email клиента (подтверждение приема заказа).
Продвинутая часть:

Экспорт товаров;
Админка заказов (проставление статуса заказа и уведомление клиента);
Выделение медленных методов в отдельные асинхронные функции (email, импорт, экспорт).
Внимание!
Поскольку в репозитории приведен готовый пример с базовой частью проекта для любого студента есть два пути:

Можно разработать свою собственную версию, исходя из текстового описания проекта
Можно взять за основу пример из репозитория, досконально изучив его, приступить к Продвинутой части
Не опасайтесь субъективно трактовать текстовое описание проекта. Работа над дипломом в первую очередь творческий процесс

Главное не сдавать работы других студентов

Исходные данные
Общее описание сервиса
Спецификация (API) - 1 шт.
Файлы yaml для импорта товаров - 1 шт.
Базовый пример API Сервиса для магазина
Этапы разработки
Разработку Backend рекомендуется разделить на следующие этапы:

Базовая часть:

Создание и настройка проекта
Проработка моделей данных
Реализация импорта товаров
Реализация API views
Полностью готовый backend
Продвинутая часть (по желанию, если базовая часть полностью готова):

Реализация forms и views админки склада
Вынос медленных методов в задачи Celery
Создание docker-compose файла для приложения
Настоятельно рекомендуется вести разработку с использованием git (github/gitlab/bitbucket) с регулярными коммитами в репозиторий, доступный вашему дипломному руководителю. Старайтесь делать коммиты как можно чаще

Этап 1. Создание и настройка проекта
Критерии достижения:

Вы имеете актуальный код данного репозитория на рабочем компьютере;
У вас создан django-проект и он запускается без ошибок.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 2. Проработка моделей данных
Критерии достижения:

Созданы модели и их дополнительные методы.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 3. Реализация импорта товаров
Критерии достижения:

Созданы функции загрузки товаров из приложенных файлов в модели Django.
Загружены товары из всех файлов для импорта.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 4. Реализация APIViews
Критерии достижения:

Реализованы API Views для основных страниц сервиса (без админки):
Авторизация
Регистрация
Получение списка товаров
Получение спецификации по отдельному товару в базе данных
Работа с корзиной (добавление, удаление товаров)
Добавление/удаление адреса доставки
Подтверждение заказа
Отправка email c подтверждением
Получение списка заказов
Получение деталей заказа
Редактирование статуса заказа
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 5. Полностью готовый backend
Критерии достижения:

Полностью работающие API Endpoint'ы
Корректно отрабатывает следующий сценарий:
пользователь может авторизироваться;
есть возможность отправки данных для регистрации и получения email с подтверждением регистрации;
пользователь может добавлять в корзину товары от разных магазинов;
пользователь может подтверждать заказ с вводом адреса доставки;
пользователь получает email с подтверждением после ввода адреса доставки;
Пользователь может переходить на страницу "Заказы" и открывать созданный заказ.
Для получения подробностей по данному этапу перейдите по ссылке.

Полезные материалы
Информация о сервисе
Спецификация API
Описание страниц сервиса
Продвинутая часть (по желанию)
Обязательное условие: Базовая часть полностью готова.

Этап 6. Реализация API views админки склада
Критерии достижения:

Реализованы API views для страниц админки сервиса.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 7. Вынос медленных методов в задачи Celery
Критерии достижения:

Создано Celery-приложение c методами:
send_email
do_import
Создан view для запуска Celery-задачи do_import из админки.
Для получения подробностей по данному этапу перейдите по ссылке.

Этап 8. Создание docker-compose файла для приложения
Создать docker-compose файл для сборки приложения.
Предоставить инструкцию для сборки docker-образа.
