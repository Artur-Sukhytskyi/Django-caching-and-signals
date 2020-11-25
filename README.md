# Django-caching-and-signals

Дополнить сигналами проект таск-менеджера на Django и подключите страницу с кэшированием.

1. В сигналах, которые обрабатывают увеличение / уменьшение счетчика задач, замените циклы с подсчетами на увеличение / уменьшение старого значения счетчика.
2. Сделайте новый счётчик задач по приоритетам:
    а) Каждый раз, когда создаётся задача по сигналу post_save, вы обновляете счётчик приоритетов. Всего у вас будет столько же объектов, сколько приоритетов в базе.
    б) Счётчики приоритетов можно просто привязать к классу TodoItem и обрабатывать без дополнительных many2many связей.
    в) Выводите счётчики на основной странице index, где мы выводили счётчики задач с категориями.
3. Запустите ваш проект на Heroku. Не забудьте подключить кэширование, как мы это делали в модуле.
4. Создайте пользователя-администратора в проекте с логином pws_admin и паролем sf_password.
5. Добавьте view с кэшированием — это страница, на которой будет только текущее число и дата (datetime.now). Страница (и дата на ней) должна кэшироваться на 5 минут. Это значит,
   что при первом доступе на этой странице сохраняется дата, но в ближайшие 5 минут от этого она не изменяется.

Требования к проекту указаны в файле "requirements.txt"

Для запуска использовать в консоли команду: "python manage.py runserver"

После запуска сервера, проект будет доступен по адресу http://127.0.0.1:8000/

Логин от админки:  pws_admin
Пароль от админки: sf_password

Add signals to the Django task manager project and connect the page with caching.

1. In signals that handle increasing / decreasing the task counter, replace the counting loops with increasing / decreasing the old counter value.
2. Make a new task counter by priority:
    a) Every time a task is created on the post_save signal, you update the priority counter. In total, you will have as many objects as there are priorities in the database.
    b) Priority counters can be simply bound to the TodoItem class and processed without additional many2many relationships.
    c) Display counters on the main index page, where we displayed task counters with categories.
3. Run your project on Heroku. Do not forget to enable caching, as we did in the module.
4. Create an administrator user in the project with login pws_admin and password sf_password.
5. Add a cached view - this is a page with only the current date and date (datetime.now). The page (and the date on it) should be cached for 5 minutes. It means,
   that the first time you access this page, the date is saved, but in the next 5 minutes from this it does not change.

Project requirements are specified in the "requirements.txt" file

To run, use the command in the console: "python manage.py runserver"

After starting the server, the project will be available at http://127.0.0.1:8000/

Login from admin panel: pws_admin
Admin password: sf_password
