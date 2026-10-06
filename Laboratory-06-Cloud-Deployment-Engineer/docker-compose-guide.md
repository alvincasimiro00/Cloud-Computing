# Docker Compose Guide

## Services Block
All containers we create are listed here:
- **database** — MariaDB database. Stores accounts, passwords, and data.
- **app** — Nextcloud website. This is what users see and use.

## Environment Variables
Settings passed into each container automatically:
- **database** — Sets passwords and database name, no manual setup needed
- **app** — Tells Nextcloud the login details and where to find the database

## MYSQL_HOST=database
Both containers share the same network. The name `database` works like an address — Nextcloud finds it automatically. No IP address needed.

## Commands Explained
- **docker-compose up -d** — Starts everything at once. Runs in the background so you can still use your terminal.
- **docker-compose down** — Stops and removes all containers and networks. Clean and complete.
- Using this file means **one command does it all** — no typing long commands over and over.
