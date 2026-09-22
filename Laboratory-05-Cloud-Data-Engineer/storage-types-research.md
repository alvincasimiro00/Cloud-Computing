Cloud Storage Types Research

Comparison of Storage Types

| Feature | Block Storage | File Storage | Object Storage |
|---|---|---|---|
| Description | Data split into fixed-size blocks, each stored with its own address. Behaves like a physical hard drive; mounted to an operating system. | Data organized in a hierarchical folder-and-file structure. Accessed through file paths; shared by multiple users/systems. | Data stored as independent "objects" — each with content, unique ID, and metadata. Stored in flat containers called buckets. |
| Primary Use Case | Databases, boot disks, transactional systems — fast low-level read/write. | Shared drives, team file storage, CMS — organized file sharing. | Photos, videos, backups, logs, big data — massive scale, direct web access. |
| Cloud Provider Example | AWS EBS, Azure Managed Disks, GCP Persistent Disk | AWS EFS, Azure Files, GCP Filestore | AWS S3, Azure Blob Storage, GCP Cloud Storage |

 Recommendation for the Client

For your photo-sharing application, Object Storage is the best choice. It scales infinitely to handle millions of images without slowing down, and every photo gets its own direct web link so users can access it instantly. Unlike block or file storage, it was built from the ground up to store and serve huge amounts of unstructured media efficiently and affordably.
