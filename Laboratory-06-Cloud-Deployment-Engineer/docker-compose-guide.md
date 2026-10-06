# Docker Compose Guide — Nextcloud + MariaDB

## What is this file?
`docker-compose.yml` is a declarative blueprint. Instead of typing separate `docker run` commands for every container, you define your entire stack in one file — services, images, environment, ports — and Compose creates, connects, and manages everything consistently.

---

## The Configuration
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
