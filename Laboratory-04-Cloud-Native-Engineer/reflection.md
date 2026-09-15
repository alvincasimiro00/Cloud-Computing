 Reflection

Docker containers start in just seconds. Virtual Machines take several minutes to start because they load a whole new operating system. Containers share the system already installed on your computer, so they are much faster and lighter.

Port mapping is needed because containers run separately from your computer. Services inside the container cannot be reached directly. Using -p 8080:80 means that when you open port 8080 on your computer, it connects to port 80 inside the container where the Nginx web server runs.

When you use docker rm, the container is removed completely along with anything saved inside it. The original image file you used to create the container stays on your computer and can be used again.

Containerization helps teams work better. It ensures the app runs exactly the same way on every computer and server. This removes common setup problems, makes deployment faster, and helps applications scale easily.

My GitHub portfolio is becoming more organized with each activity. It now has clear folders, files, and screenshots showing what I have done. It serves as a record of what I am learning and my progress in cloud computing.
