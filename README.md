# [Strapi](https://github.com/strapi/strapi) containerized

![Strapi](https://cldup.com/7umchwdUBh.png)

API creation made simple, secure and fast.
The most advanced open-source Content Management Framework to build powerful API with no effort.

***
## Warning❗️
The original repo has content type builder's bug (older nodejs)
This fork fixed that problem ✌🏻

## Quickstart (Fully Recommended)

1. `git clone https://github.com/Rminsh/strapi-docker && cd strapi-docker`
2. Run using `docker-compose up`
3. After strapi has completeled the setup , press `ctrl + c`
4. Then find docker composer id via `sudo docker ps -a`
5. run mongodb docker and strapi docker via `sudo docker start <docker-id>`


## Use as base image

```Dockerfile
FROM strapi/strapi
```

## Environment variables

- `APP_NAME` to override the `strapi-app` generated folder name (you should also update the volumes paths).
- `DATABASE_CLIENT` a database providers supported by Strapi: MongoDB, Postgres, MySQL, Sqlite3 and Redis.
- `DATABASE_HOST` database service name.
- `DATABASE_PORT` depends on your database client.
- `DATABASE_NAME` initializes a database with specific name (default strapi). When using MongoDB, you should also update the `MONGO_INITDB_DATABASE` environment in the db service.
- `DATABASE_USERNAME` set the username of the database connection.
- `DATABASE_PASSWORD` set the password of the database connection.
- `DATABASE_SSL` boolean for SSL.
- `DATABASE_AUTHENTICATION_DATABASE` set the authentification.
