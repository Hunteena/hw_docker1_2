# Задание 2 к лекции Docker

Создание образа (из папки с Dockerfile и /stocks_products):

```$ docker build --tag stocks_products .```

Создание тома для базы данных:

```$ docker volume create db_volume```

Запуск контейнера с подключенным томом:

```$ docker run --name stocks_products_runned -p 8000:8000 --mount source=db_volume,target=/stocks_products/db stocks_products```

Сервер будет доступен по адресу http://localhost:8000/api/v1/
