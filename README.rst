TTA - Time Tracker Autocomplete tool
================================================

.. image:: https://badges.gitter.im/Join%20Chat.svg
   :alt: Join the chat at https://gitter.im/erm0l0v/tta
   :target: https://gitter.im/erm0l0v/tta?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge

.. image:: https://img.shields.io/pypi/v/tta.svg
    :target: https://pypi.python.org/pypi/tta
    :alt: Latest PyPI version

.. image:: https://requires.io/github/erm0l0v/tta/requirements.svg?branch=master
     :target: https://requires.io/github/erm0l0v/tta/requirements/?branch=master
     :alt: Requirements Status

.. image:: https://landscape.io/github/erm0l0v/tta/master/landscape.svg?style=flat
   :target: https://landscape.io/github/erm0l0v/tta/master
   :alt: Code Health
   

Автозаполнялка Time Tracker-а для Murano Soft. Тулза использует этот `API <http://basicdata.ru/api/calend/>`_ для определения рабочих и не рабочих дней.


Запуск в docker:
----------

Тулза запаковывается в docker-образ и заливается на github. Пример запуска:

.. code::

    docker run --rm -it --entrypoint tta appulate/tta:latest -u ivan.petrov -c 14 -p MySuperDomainPassword -m "Super Job"
    
Обратите внимание на параметры -c и -m. Они задают категорию и комментарий для tt. Более подробное описание ниже.


Параметры:
--------


+----------------------------+--------------------------------------------+
| Option                     | Description                                |
+=======+====================+============================================+
| *-u*  | *--user*           | логин от Time Tracker                      |
+-------+--------------------+--------------------------------------------+
| *-p*  | *--password*       | пароль от Time Tracker                     |
+-------+--------------------+--------------------------------------------+
| *-m*  | *--message*        | комментарий к записи в Time Tracker        |
+-------+--------------------+--------------------------------------------+
|       | *--start_date*     | Начало периода (Пример: 2015-8-27)         |
|       |                    |                                            |
|       |                    | *По дефолту:*                              |
|       |                    | *первый день текущего месяца*              |
|       |                    |                                            |
+-------+--------------------+--------------------------------------------+
|       | *--end_date*       | Окончание периода (Пример: 2015-8-29)      |
|       |                    |                                            |
|       |                    | *По деволту:*                              |
|       |                    | *последний день текущего месяца*           |
|       |                    |                                            |
+-------+--------------------+--------------------------------------------+
|       | *--start_work_day* | Начало рабочего дня (часы).                |
|       |                    |                                            |
|       |                    | По дефолту: *10*.                          |
+-------+--------------------+--------------------------------------------+
|       | *--end_work_day*   | Конец рабочего для (часы).                 |
|       |                    |                                            |
|       |                    | По дефолту: *18*.                          |
+-------+--------------------+--------------------------------------------+
| *-c*  | *--category*       | Категория в Time Tracker                   |
|       |                    |                                            |
|       |                    | *По дефолту: 2 (Development)*.             |
|       |                    +--------------------------------------------+
|       |                    | **Список категорий:**                      |
|       |                    +----+---------------------------------------+
|       |                    | ID | Name                                  |
|       |                    +----+---------------------------------------+
|       |                    | 17 | Client Support                        |
|       |                    +----+---------------------------------------+
|       |                    | 12 | Code Review                           |
|       |                    +----+---------------------------------------+
|       |                    | 2  | Development                           |
|       |                    +----+---------------------------------------+
|       |                    | 4  | Documenting                           |
|       |                    +----+---------------------------------------+
|       |                    | 15 | Graphic Design                        |
|       |                    +----+---------------------------------------+
|       |                    | 27 | Holiday                               |
|       |                    +----+---------------------------------------+
|       |                    | 29 | HR                                    |
|       |                    +----+---------------------------------------+
|       |                    | 14 | Infrastructure                        |
|       |                    +----+---------------------------------------+
|       |                    | 28 | Marketing                             |
|       |                    +----+---------------------------------------+
|       |                    | 7  | Meeting                               |
|       |                    +----+---------------------------------------+
|       |                    | 8  | Miscellaneous                         |
|       |                    +----+---------------------------------------+
|       |                    | 30 | Office Management                     |
|       |                    +----+---------------------------------------+
|       |                    | 35 | Overtime leave                        |
|       |                    +----+---------------------------------------+
|       |                    | 9  | Project Management                    |
|       |                    +----+---------------------------------------+
|       |                    | 10 | Quality Assurance/Testing             |
|       |                    +----+---------------------------------------+
|       |                    | 3  | Requirement Analysis                  |
|       |                    +----+---------------------------------------+
|       |                    | 6  | Research                              |
|       |                    +----+---------------------------------------+
|       |                    | 25 | Sick                                  |
|       |                    +----+---------------------------------------+
|       |                    | 31 | Vacation non-paid                     |
|       |                    +----+---------------------------------------+
|       |                    | 26 | Vacation paid                         |
+-------+--------------------+----+---------------------------------------+


`tta` was written by `Kirill Ermolov <erm0l0v@ya.ru>`_.
