Kittygram - сайт для того чтоб делиться своими питомцами.

### Технологический стек:
+ Python 3.9
+ Django
+ Django REST Framework
+ SimpleJWT
+ PostgeSQL
+ Nginx
+ Docker

### Потребуется файл .env:
  + В нем должны быть:
```
      DOMAIN_NAME -- доменное имя вашего сервера
      IP_SERVER -- IP вашего сервера
      IP_LOCAL --  Локальный IP вашего сервера

      SECRET_KEY -- секретный ключ от django
      DB_HOST -- db
      DB_PORT -- Порт подключения к базе данных
      POSTGRES_DB -- название вашей базы данных
      POSTGRES_USER -- Имя пользователя для запросов в базу
      POSTGRES_PASSWORD -- Пароль пользователя для запросов в базу
```

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

### Автор :
+ [Бесчастный Сергей](https://github.com/Domenen)
