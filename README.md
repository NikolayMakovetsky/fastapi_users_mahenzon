## Lesson 01 / preparation / Подготовка к работе

#### Склонировать репозиторий
```
git clone https://github.com/mahenzon/FastAPI-base-app.git
```
Данную команду не получилось исполнить в терминале PyCharm,
т.к. он не видел символы ВЕРХНЕГО РЕГИСТРА, из-за чего
передавался неверный адрес проекта (ast вместо FastAPI)
Чтобы решить проблему, воспользовался Командной строкой Win

#### Альтернативые варианты склонировать репозиторий
1. Скачать ZIP файл с проектом
2. Использовать команду RESET

Для этого нужно сначала проинициализировать новый пустой репозиторий,
указать адрес удаленного репозитория: [ссылка](https://github.com/mahenzon/FastAPI-base-app.git)
,после чего сделать на него RESET

#### Откат проекта до нужного комита (Add sources urls)

> RightClick -> Reset Current Branch to Here...(Hard)

[read about git reset](https://www.studytonight.com/git-guide/git-reset#:~:text=Git%20Reset%20%2D%2Dsoft.%20The%20%2D%2Dsoft,changes%20in%20the%20staging%20area)

Основные понятия:
1. Рабочая директория (Working tree)
2. Поле отслеживания (Staging area)
Файл попадает сюда после команды Add

3. Локальный репозиторий (Repository)
Файл (в своем текущем состоянии) попадает сюда после команды Comit

#### Удаление удаленной ветки origin master

(Делаем это, чтобы отключиться от удаленного репозитория)
1. Переносим скрытую папку .git, а также .gitignore в корень проекта
2. Получаем список связей нашего репозитория
```
git remote (выясняем куда "смотрит" наш гит) -> origin
```
3. Удаляем ненужную связь
```
git remote remove origin (удаление связи)
```
В результате осталась только локальная ветка master

#### Пометить папку fastapi-application как рабочую папку

fastapi-application -> Mark Directore as -> Sources Root

Именно из этой папки мы дальше будем все импортировать, и нужно
чтобы PyCrarm понимал, что это корень нашего проекта! Т.е. запуская
main.py мы хотим запускаться как будто находимся в 
fastapi-application

#### Установка зависимостей ВО (poetry)

#### Запуск docker-compose.yml

Предназначен для работы с БД Postgres

Можно подключаться к БД через Adminer, pgadmin...или вы можете
использовать другие инструменты (DBeaver - тоже хороший бесплатный инструмент)

Если есть возможность работать в PyCharm PRO, то здесь можно
подключаться к БД через инструмент "Database", с которым
очень удобно работать прямо в PyCharm не переключаясь

```
docker compose up -d pg
```
```
docker compose ps (убедимся, что сервис запустился)
```

#### Начинаем работу с FastAPI Users

[Fastapi users Docs](https://fastapi-users.github.io/fastapi-users/latest/)
