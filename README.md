# Описание
Первый проект [@PythonNoobs](https://t.me/python_noobs)
help_desk &amp; service_desk system

# Requirements / Требования
Django==1.11.15

# Installation / Установка
- Open the command line, navigate to the django app folder and execute:
- virtualenv *virtualenvname*
- Clone this repository to virtualenv folder
- Linux: source *virtualenvname*/bin/activate, Windows: call *virtualenvname*/Scripts/activate.bat
- pip install -r requirements.txt
- move to cloned repository folder
- python manage.py makemigrations
- python manage.py migrate
- django-admin createsuperuser *username*
- python manage.py runserver
- Open http://127.0.0.1:8000/ in web browser.

# Основные подсистемы и требования:
- Подсистема регистрации\авторизации (authapp)
- Система заявок(ticketsapp)
- Реестр пользователей(employeesapp)
- Реестр серверов(serverapp)
- Реестр копировально-множительной техники(КМТ)(cmtapp)
- Реестр компьютеров(workstationsapp)
- Реестр USB-флеш носителей (flashcardsapp)
- Реестр USB-флеш носителей (tokensapp)
- Подсистема администрирования(adminapp)
- Подсистема новостей(newsapp)

## Общие требования к реализации всех приложений:
- модели должны быть реализованы в соответствии со схемой БД. (в схеме возможны опечатки и неточности. Дополнительно спрашивайте в чате). Для каждой модели обеспечить корректное отображение в административной панели джанго: название модели, название объектов модели и так далее (class Meta).
- описание форм и их вывод в шаблон разрешается реализовать любым удобным(доступным) для вас способом: обычные формы или формы на основе моделей. Формы должны соответствовать стилю определенному в проекте.
- контроллеры (views) разрешается реализовать любым удобным для вас способом: обычные или CBV. 


## Система заявок(ticketsapp)
Модели приложения:
- Ticket
- MainProblem
- SubProblem

Реализовать(основное):
- страница создания новой заявки. На странице указываются общая проблема, ее категория, описание, статус. При выборе проблем связанных с компьютером, сервером, или КМТ, должна осуществляться привязка к соответствующей модели.
- страница изменения заявки
- страница всех зарегистрированных в системе заявок. Вывод информации осуществляется в табличном виде всех зарегистрированных заявок с указанием параметров определенных в модели

Реализовать(дополнительно):
-Дату выводить в определенном формате "день-месяц-год часы-минуты"
-Реализовать зависимости подпроблем от проблем(Ajax). Т.е. к примеру, при выборе общей проблемы "Серверы", в меню "подпроблемы" дожны быть перечислены только "подпроблемы" относящиеся к серверам.
-Выделить заявки цветом в зависимости от их статуса(в работе - оранжевым, выполненные - зелёным, открытые - без цвета)
-при создании заявки автоматически добавлять в заявку создавшего ее пользователя.
-на панели навигации указывать общее количество заявок назначенных пользователю, количество открытых заявок и заявки в работе.

## Реестр пользователей(employeesapp)
Модели приложения:
- Employee
- Post
- Department 
- SubDevision

Реализовать(основное):
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.
- страница "телефонный справочник". На странице отображать данные всех сотрудников.
- страница "дни рождения сотрудников". На странице отображать фото, ФИО, дни рождения сотрудников. Дни рождения отсортировать от ближайшего дня рождения к текущей дате. Отображение дня рождения реализовать в формате "день месяц" на странице "дни рождения сотрудников"

Реализовать(дополнительно):
- Импорт данных в базу через таблицу Excel
- Строки в таблице, где дни рождения наступили сегодня подсвечивать зеленым цветом, дни рождения в ближайшие 3 дня подсвечивать желтым цветом.
- Реализовать добавление фото сотрудника. Фото отображать во всех списках и карточке сотрудника.

## Реестр серверов(serverapp)
Модели приложения:
- Server
- ServerModel

Реализовать(основное):
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. - Предусмотреть возможность возможность удаления карточки позиции.

Реализовать(дополнительно):
- Импорт данных в базу через таблицу Excel
- Реализовать проверку доступности серверов с помощью команды ping по указанным IP-адресам.
- Подсвечивать серверы в списке различными цветами (доступные - зеленым цветом, недоступные - красным)

## Реестр копировально-множительной техники(КМТ)(cmtapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

Реализовать(дополнительно):
- Импорт данных в базу через таблицу Excel

## Реестр компьютеров(workstationsapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

Реализовать(дополнительно):
- Импорт данных в базу через таблицу Excel
- Реализовать проверку доступности серверов с помощью команды ping по указанным IP-адресам.

## Реестр USB-флеш носителей (flashcardsapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

Реализовать(дополнительно):
- Импорт данных в базу через таблицу Excel

## Реестр USB-флеш носителей (tokensapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

Реализовать(дополнительно):
- Импорт данных в базу через таблицу Excel

## Подсистема администрирования(adminapp)
-в настоящий момент требования не определены

## Подсистема авторизации(authapp)
- страница личного кабинета сотрудника
- страница с формой регистрации пользователя
- страница с формой входа пользователя

## Схема БД / DB schema:
[Схема БД на sqldbm.com](https://app.sqldbm.com/MySQL/Share/GfsY_w-ltzIsuKaV2wf9XEGFrngIE8md_DYjF4jNYw0)
