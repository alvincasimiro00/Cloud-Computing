# Two-Tier Architecture

## The Web/Application Tier

This is the part of the system that users see and use. It handles the website, file uploads and downloads, and other functions of Nextcloud. It also connects to the database when it needs information.

## The Database Tier

This is where the important information is stored. It includes user accounts, file information, permissions, and system settings. The database gets requests from the application and sends back the needed information.

## Why Separate Them?

Separating the web and database makes the system easier to manage.

* **Easy to scale** – the web part can be increased if more users use the system.
* **Better performance** – each part has its own job.
* **Easy to update** – one part can be changed without affecting the whole system.
* **Better security** – the database can be kept private.
* **Easy to maintain** – problems can be easier to find and fix.

If both are placed in one container, the system can be harder to manage, update, and secure.
