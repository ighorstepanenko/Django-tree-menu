# Описание

Данный проект является django-app, который реализует древовидное меню, позволяет вносить в БД меню (одно или несколько) через админку и нарисовать на любой нужной странице меню по названию.

# Требования

В качестве СУБД используется sqlite3, проект будет развёрнут с помощью Docker-Compose, который входит в состав Docker (Скачать Docker можно по [ссылке](https://docs.docker.com/get-docker/)). Используемые библиотеки хранятся в файле requirements.txt.

# Развертывание приложения

Для того, чтобы развернуть приложение, нужно:

1) скопировать файлы в локальную директорию с помощью команды

  $ git clone https://github.com/ighorstepanenko/Django-tree-menu.git

2) перейти в скопированную директорию и развернуть приложение в Docker-Compose, для этого необходимо выполнить следующие команды:

  $ cd Django-tree-menu/ && sudo docker compose up -d

> Если пишет, что данный адрес уже используется, то просмотрите с помощью команды `sudo ss -lptn 'sport = :<PORT>'` какой процесс использует данный адрес и остановите процесс с помощью команды `sudo kill -KILL <PID>' либо измените в файле Docker-compose первый порт с "8000" на любой свободный в команде строке 'ports'

3) перейти в браузере по адресу http://localhost:8000/admin (либо http://localhost:<прописанный вами порт>/admin )

4) ввести логин 'admin', пароль '1111'
