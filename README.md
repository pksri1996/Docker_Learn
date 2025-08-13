🐳 Docker Conceptual Overview & Example Project
This repository provides a small working project to help understand Docker at a conceptual level. It demonstrates how to create images and run containers using Docker, with a Node.js backend and MongoDB.

💡 Conceptual Overview
🖥️ Docker is OS without kernel

Provides an isolated environment for applications to run consistently across machines.

🏗️ Build Docker Image using Dockerfile

Contains instructions on base image, dependencies, and commands to create the image.

📦 Image = Blueprint for Containers

Once built, it can be used to spawn multiple containers.

🚀 Run containers using docker-compose.yml

Defines which containers to start, their ports, volumes, and environment variables.

🔄 Start required containers for your app

Ensures all components run properly and can communicate with each other.

📜 Dockerfile details

Commands tell Docker what to download, which image to create, and what commands to run during build.

⚙️ docker-compose.yml details

Sets up images, versions, ports, passwords (if any), and public access ports.

📈 Kubernetes (future)

Optional: used to auto-scale containers based on traffic or health.

🛠️ How to Use
Clone the repository

```bash
git clone https://github.com/pksri1996/Docker_Learn.git
cd Docker_Learn

```
Build & run containers


```bash
docker-compose up --build

```
🔹 Builds Node.js backend image from Dockerfile

🔹 Starts a MongoDB container

🔹 Connects backend to MongoDB using environment variables in docker-compose.yml

Access the application

🌐 Backend API → http://localhost:5000

💾 MongoDB data persists in Docker volume (mongo_data), so data is safe even if the container restarts.

Test the example routes

POST /api/books → Add a book:

```json

{
  "title": "Book Title",
  "author": "Author Name",
  "genre": "Fiction"
}
```

GET /api/books → Retrieve all books.

Stop containers

```bash
docker-compose down

```
This setup gives a simple but complete environment for experimenting with Docker, building images, and running multiple containers with a single command.
