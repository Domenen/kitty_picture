![Kittygram](https://github.com/github/docs/actions/workflows/main.yml/badge.svg) - сайт для того чтоб делиться своими питомцами. Вы можете выложить фотографию своего питомца , так же указать его достижения. Можете посмотреть на питомцев других людей.

### Технологический стек:
+ Python 3.9
+ Django
+ Django REST Framework
+ SimpleJWT
+ PostgeSQL
+ Nginx
+ Docker

### Как запустить проект:
  + Установить Docker
  + Скачать из данного репозитория файл docker-compose.production.yml
  + Далее находять в той же дириктории выполнить команды :
```
          docker compose -f docker-compose.production.yml up -d
          docker compose -f docker-compose.production.yml exec backend python manage.py migrate
          docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
          docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```

### Потребуется файл .env:
  + В нем должны быть:
```
      ALLOWED_HOSTS -- IP вашего сервера и доменное имя, через запятую

      SECRET_KEY -- секретный ключ от django
      DB_HOST -- db
      DB_PORT -- Порт подключения к базе данных
      POSTGRES_DB -- название вашей базы данных
      POSTGRES_USER -- Имя пользователя для запросов в базу
      POSTGRES_PASSWORD -- Пароль пользователя для запросов в базу
```


### Автор :
+ [Бесчастный Сергей](https://github.com/Domenen)
