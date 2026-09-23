 MinIO Object Storage Deployment

 Mission Overview
This activity deploys a self-hosted S3-compatible Object Storage server (MinIO) using Docker, creates a bucket named `client-photos`, and demonstrates file upload capability — providing scalable, reliable storage suitable for a photo-sharing application.

 Objectives
- Differentiate between Block, File, and Object Storage
- Deploy MinIO using Docker
- Access MinIO Console via web browser through port forwarding
- Create a bucket and upload objects
- Document the process using Markdown

 Tools Used
- KillerCoda Playground — Ubuntu/Docker environment
- Docker — Container runtime
- MinIO — Open-source S3-compatible object storage server
- Web Browser — MinIO Console access

 Deployment Steps

 Step 1: Run MinIO Docker Container
Execute this command in the KillerCoda terminal:
```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
quay.io/minio/minio server /data --console-address ":9001"
