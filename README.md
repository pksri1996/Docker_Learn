Docker Conceptual Overview & Example Project
This repository provides a small working project to help understand Docker at a conceptual level. It demonstrates how to create images and run containers using Docker, with a Node.js backend and MongoDB.

Conceptual Overview
Docker is OS without kernel — it provides an isolated environment for applications to run consistently across machines.

We need to first make a Docker image using Dockerfile — this file contains instructions on how to build the image, including which base image to use, dependencies to install, and commands to run.

The image defines the blueprint for containers — once built, it can be used to spawn multiple containers.

Once the image is built, we run the docker-compose.yml file — it defines which containers to start, their configurations, ports, volumes, and environment variables.

This will start the number of containers required for the application to run properly.

Dockerfile commands tell Docker what to download, which image to create, and what commands to run before creating the image.

docker-compose.yml sets up all images, their versions, ports, passwords if any, along with which ports to open for public access.

Kubernetes (optional, future learning) — can be used to auto-scale containers, creating new ones or shutting down old ones based on traffic or container health.

How to Use
Follow these steps to get the project running locally:

Clone the repository

bash
Copy
Edit
git clone https://github.com/pksri1996/Docker_Learn.git
cd Docker_Learn
Build and run containers using Docker Compose

bash
Copy
Edit
docker-compose up --build
This will:

Build the Node.js backend image from the Dockerfile.

Start a MongoDB container.

Connect the backend to MongoDB using the environment variables defined in docker-compose.yml.

Access the application

Backend API will be available at http://localhost:5000.

MongoDB data is persisted in a Docker volume (mongo_data) so data will not be lost if the container is restarted.

Test the example routes

POST /api/books → Add a book with JSON body:

json
Copy
Edit
{
  "title": "Book Title",
  "author": "Author Name",
  "genre": "Fiction"
}
GET /api/books → Retrieve all books.

Stop containers

bash
Copy
Edit
docker-compose down
This setup gives a simple but complete environment for experimenting with Docker, building images, and running multiple containers with a single command.
