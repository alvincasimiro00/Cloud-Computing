 Mission Reflection

Docker containers boot and become ready in seconds, whereas starting an operating system on a Virtual Machine takes several minutes. This happens because containers share the host operating system instead of loading a full separate system of their own.

Port mapping is necessary when running a web server inside a container because the container runs in an isolated network space. By using `-p 8080:80`, traffic from port 8080 on your local computer is forwarded to port 80 inside the container, where the Nginx web server listens.

When you use the `docker rm` command, the container itself and all changes made inside it are permanently deleted. The original image file that you used to create the container remains available and unchanged on your system.

Containerization changes how software developers and IT operations teams work together. It provides consistent environments from development through testing and production. This removes common compatibility issues, speeds up deployment, and makes applications easier to scale and maintain.

My GitHub portfolio continues to grow as an organized collection of my work and progress. Each laboratory activity adds properly structured folders, documentation, and evidence of tasks completed. It serves as a clear, permanent record of the skills I have learned and the work I have accomplished.
