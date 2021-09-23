# Приложение Pingrobot для мониторинга определенного пула ресурсов с заданым интервалом
## Из Недели #2 курса GOLANG NINJA

### Стэк
- go 1.17
- postgres 

### Запуск
Для запуска необходимо указать переменные окружения, например в файле .env

```
export DB_HOST=localhost
export DB_PORT=5432
export DB_USERNAME=postgres
export DB_NAME=postgres
export DB_SSLMODE=disable
export DB_PASSWORD=qwerty123
```

Сборка и запуск
```
source .env && go build -o app cmd/main.go && ./app
```

Для postgres можно использовать Docker

```
docker run -d --name ninja-db -e POSTGRES_PASSWORD=qwerty123 -v ${HOME}/pgdata/:/var/lib/postgresql/data -p 5432:5432 postgres
```