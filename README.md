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
- Система заявок(ticketsapp)
- Реестр пользователей(employeesapp)
- Реестр серверов(serverapp)
- Реестр копировально-множительной техники(КМТ)(cmtapp)
- Реестр компьютеров(workstationsapp)
- Реестр USB-флеш носителей (flashcardsapp)
- Реестр USB-флеш носителей (tokensapp)

## Система заявок(ticketsapp)
Реализовать:
- страница создания новой заявки. На странице указываются общая проблема, ее категория, описание, статус. При выборе проблем связанных с компьютером, сервером, или КМТ, должна осуществляться привязка к соответствующей модели.
- страница изменения заявки
- страница всех зарегистрированных в системе заявок. Вывод информации осуществляется в табличном виде всех зарегистрированных заявок с указанием параметров определенных в модели

## Реестр пользователей(employeesapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.
- страница "телефонный справочник"
- страница "дни рождения сотрудников"

## Реестр серверов(serverapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

## Реестр копировально-множительной техники(КМТ)(cmtapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

## Реестр компьютеров(workstationsapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.


## Реестр USB-флеш носителей (flashcardsapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.

## Реестр USB-флеш носителей (tokensapp)
Основные требования:
- страница с выводом всех зарегистрированных позиций. Вывод информации на страницу реализовать в табличном виде с выводом всех параметров определенных в модели. Вывод данных осуществить с помощью библиотеки datatables(datatables.net), файлы которой уже добавлены в статические файлы проекта. Если не используется библиотека datatables, вывести данные через стандартную таблицу с применением пагинации страниц и бутстрап стилей.
- страница добавления новой позиции.  На страницу вывести форму с полями соответствующими параметрам определенным в модели.
- страница редактирования карточки существующей позиции. На страницу вывести форму для редактирования параметров определенных в модели. Предусмотреть возможность возможность удаления карточки позиции.


## Подсистема администрирования(adminapp)
-в настоящий момент требования не определены

## Подсистема авторизации(authapp)
- страница личного кабинета сотрудника
- страница с формой регистрации пользователя
- страница с формой входа пользователя

## Схема БД / DB schema:
[Схема БД на sqldbm.com](https://app.sqldbm.com/MySQL/Share/GfsY_w-ltzIsuKaV2wf9XEGFrngIE8md_DYjF4jNYw0)
