In this DevOps task, you need to build and deploy a full-stack CRUD application using the MEAN stack (MongoDB, Express, Angular 15, and Node.js). The backend will be developed with Node.js and Express to provide REST APIs, connecting to a MongoDB database. The frontend will be an Angular application utilizing HTTPClient for communication.  

The application will manage a collection of tutorials, where each tutorial includes an ID, title, description, and published status. Users will be able to create, retrieve, update, and delete tutorials. Additionally, a search box will allow users to find tutorials by title.

## The objective of this task was to:

1.Containerize frontend and backend using Docker

2.Use Docker Compose for multi-container orchestration

3.Implement CI/CD using GitHub Actions

4.Push images to Docker Hub

5.Deploy the application on AWS EC2

6.Configure Nginx reverse proxy on port 80

## Project setup

### Node.js Server

cd backend

npm install

You can update the MongoDB credentials by modifying the `db.config.js` file located in `app/config/`.

Run `node server.js`

### Angular Client

cd frontend

npm install

Run `ng serve --port 8081`

You can modify the `src/app/services/tutorial.service.ts` file to adjust how the frontend interacts with the backend.

Navigate to `http://localhost:8081/`


## 🐳 Docker Setup
# Backend

-> Built with Node.js & Express

-> Runs on port 8080

-> Connected to MongoDB container

-> Dockerized using custom Dockerfile

# Frontend

-> Built using Angular 15

-> Production build served using Nginx

-> Runs on port 80

-> Multi-stage Docker build used

# Database

-> MongoDB official Docker image

-> Persistent volume attached for data storage

## 📦 Docker Hub Images

# The following images are built and pushed automatically via CI/CD:

1.praveengowda123/mean-backend:latest

2.praveengowda123/mean-frontend:latest

## CI/CD Pipeline – GitHub Actions

# Trigger

1.Automatically runs on push to main branch.

2.Pipeline Steps

3.Checkout source code

4.Build Docker images (frontend & backend)

5.Push images to Docker Hub

6.SSH into EC2 instance

7.Stop and remove old containers

8.Pull latest Docker images

9.Restart services using docker-compose

10.Deployment is fully automated.

## Nginx Reverse Proxy

1.Angular frontend served using Nginx

2.Application accessible on port 80

3.Backend runs internally on port 8080

4.HTTPS not configured (as per project requirement)

## Technologies Used

1.MongoDB

2.Express.js

3.Angular 15

4.Node.js

5.Docker

6.Docker Compose

7.GitHub Actions

8.AWS EC2

9.Nginx