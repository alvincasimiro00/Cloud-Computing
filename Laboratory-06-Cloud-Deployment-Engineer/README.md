# Laboratory 06: Cloud Deployment Engineer
**Course:** CCM101 – Cloud Computing
**Institution:** University of Eastern Pangasinan
**Student:** Casimiro, Alvin Tarangco.

---

## Mission Overview
This mission transitions from manual container deployment to **Infrastructure as Code (IaC)** using Docker Compose. We deploy a two‑tier private cloud storage stack — Nextcloud + MariaDB — with a single declarative configuration file, demonstrating how senior engineers manage infrastructure through code rather than one‑off commands.

## Objectives
- Explain multi‑tier / two‑tier application architecture
- Understand `docker-compose.yml` structure and purpose
- Use `nano` to write YAML configuration
- Deploy Nextcloud + MariaDB multi‑container stack
- Document IaC procedures in Markdown
- Maintain professional GitHub Cloud Computing Portfolio

## Commands Executed
```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
