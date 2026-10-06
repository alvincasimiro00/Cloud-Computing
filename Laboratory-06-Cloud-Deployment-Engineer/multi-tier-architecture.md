## Two-Tier Architecture

## Web and Application Tier
This is the front part — the Nextcloud page that users see. It shows files, handles uploads and downloads, and takes requests from the browser. It connects the user to the database in the background.

## Database Tier
This is the back part — the MariaDB that stores all the important information: accounts, passwords, file lists, and permissions. Users never see this directly. Only the application talks to it.

## Why Keep Them Separate?
Security — The database stays private. It is not exposed to everyone on the internet.
Easy to update — You can change or fix the application without touching the stored data.
Reliability — If one part has a problem, the other part keeps working.
Cleaner setup — Each part does one job well, and it is easier to check or fix things.

Putting them in one container would make everything messy. A problem in one part could break everything else. Separating them is the standard and safe way to build systems.
