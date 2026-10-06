# Two‑Tier Architecture

## The Web/Application Tier
This is the **frontend** — the Nextcloud web interface users interact with directly. It handles HTTP requests, renders the user interface, manages file uploads/downloads, and runs application logic. It presents the private cloud experience to the browser and communicates with the database tier behind the scenes.

## The Database Tier
This is the **backend** — the MariaDB container. It stores persistent, structured data: user accounts, credentials, file metadata, permissions, and configuration settings. It does not serve content directly to users; it responds only to queries from the application tier.

## Why Separate Them?
Separating into two distinct containers offers major advantages:
- **Independent scaling** — if traffic grows, you can replicate the web tier without touching the database
- **Specialized optimization** — database servers and web servers have different performance, security, and backup needs
- **Technology independence** — you can upgrade, replace, or migrate one component without rebuilding the whole system
- **Fault isolation** — a web app crash won’t corrupt stored data; database maintenance won’t necessarily interrupt the frontend
- **Security** — database can be restricted to internal network only, never exposed publicly
- **Maintainability** — clearer responsibility boundaries make code easier to debug and update

Packing both into one container creates a "monolith" that loses all these benefits — harder to scale, secure, update, or recover.
