![Django workflow](https://github.com/belinskii1/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)
## Учебный проект 15 спринта. Docker, контейнеризация.

### Cтек технологий:
Python 3.7+, Django 2.2+, DRF, JWT, Docker, Nginx


### Запуск проекта:

**Клонировать репозиторий и перейти в него в командной строке:**

`git clone https://github.com/Belinskii1/infra_sp2.git`
`cd api_yamdb/`

**Cоздать и активировать виртуальное окружение:**

`python3 -m venv env`
`source env/bin/activate`
`python3 -m pip install --upgrade pip`

**Установить зависимости из файла requirements.txt:**

`pip install -r requirements.txt`

**Запустить приложение в контейнерах:**

из директории infra/

`docker-compose up -d --build`

**Выполнить миграции:**

из директории infra/

`docker-compose exec web python manage.py migrate`

**Создать суперпользователя:**

из директории infra/

`docker-compose exec web python manage.py createsuperuser`

**Собрать статику:**

из директории infra/

`docker-compose exec web python manage.py collectstatic --no-input`

**Остановить приложение в контейнерах:**

из директории infra/

`docker-compose down -v`

**Запуск pytest:**

при запущенном виртуальном окружении

`cd infra_sp2 && pytest`

**Документация API с примерами:**
/redoc/  
шаблон наполнения env-файла  
см.  
infra/.env.template  
описание команды для заполнения базы данными  
`cd api_yamdb && python manage.py loaddata ../infra/fixtures.json`  

### Автор:
Семенюк Александр [belinskii1](https://github.com/Belinskii1)