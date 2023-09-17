# Kittygram

Сайт-блог для публикации ваши котов и их достижений.

## Установка

Скачиваем файл docker-compose.production.yml в отдельную новую папку

Запускаем файл в папке проекта

```bash
sudo docker compose -f docker-compose.production.yml up
```

Выполняем миграции и собираем статические файлы

```bash
sudo docker compose -f docker-compose.production.yml exec backend python manage.py migrate
sudo docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
sudo docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /static/static/
```

После запуска проект будет доступен по локальному адресу:

http://localhost:9000/

## Использование

Для использования приложения необходимо зарегистрироваться и войти на сайт.

Для добавления кота в правом в верхнем углу после входа появится соответствующая кнопка.

Можно загрузит фото кота и указать его имя, год рождения и достижения.

Достижения кота можно выбирать из существующего списка или создать новые.