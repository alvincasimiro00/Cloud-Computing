Docker Compose Guide

Services Block
All containers we create are listed here:
- database — MariaDB database. Stores accounts, passwords, and all stored information.
- app — Nextcloud website. This is the page users see and use in their browser.

Environment Variables
Settings that get passed into each container automatically:
- database — Sets passwords and the database name, so no manual setup is needed
- app — Tells Nextcloud the login details and where to find the database

How Nextcloud Finds the Database
Both containers share the same network. The name database works like an address — Nextcloud finds it automatically. No need to look up or type any IP address.

Commands Explained
docker-compose up -d — Starts everything at once. Runs in the background so you can keep using your terminal.
docker-compose down — Stops and removes all containers and networks. Leaves everything clean.
Using this file means one command does it all — no typing the same long commands over and over.
