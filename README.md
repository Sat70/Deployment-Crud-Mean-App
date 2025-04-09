In this DevOps task, you need to build and deploy a full-stack CRUD application using the MEAN stack (MongoDB, Express, Angular 15, and Node.js). The backend will be developed with Node.js and Express to provide REST APIs, connecting to a MongoDB database. The frontend will be an Angular application utilizing HTTPClient for communication.  

The application will manage a collection of tutorials, where each tutorial includes an ID, title, description, and published status. Users will be able to create, retrieve, update, and delete tutorials. Additionally, a search box will allow users to find tutorials by title.

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

# 🚀 Full-Stack MEAN Application Deployment using Docker, Docker Compose & Jenkins

This project demonstrates how to **set up**, **containerize**, and **automate the deployment** of a full-stack **MEAN** (MongoDB, Express.js, Angular, Node.js) application using **Docker**, **Docker Compose**, and **Jenkins CI/CD pipelines**.

---

## 📌 Objective

To create a reliable and reproducible development and production environment for a MEAN application that:
- Uses Docker containers for each component
- Utilizes Docker Compose to orchestrate services
- Implements Jenkins pipelines for continuous integration and deployment
- Automates pulling the latest changes and restarting containers on a remote server

---

## 📁 Project Structure
Deployment-Crud-Mean-App/ │ ├── backend/ # Express.js backend API │ └── Dockerfile # Dockerfile for backend │ ├── frontend/ # Angular frontend application │ └── Dockerfile # Dockerfile for frontend │ ├── nginx/ # NGINX reverse proxy configuration │ └── default.conf # Configures routing between frontend and backend │ ├── docker-compose.yml # Defines and runs multi-container application │ └── Jenkinsfile # Jenkins pipeline configuration for CI/CD


---

## 🛠️ Technologies Used

| Component     | Technology               |
|---------------|---------------------------|
| Frontend      | Angular                   |
| Backend       | Node.js, Express.js       |
| Database      | MongoDB                   |
| Proxy Server  | NGINX                     |
| Containerization | Docker, Docker Compose |
| CI/CD         | Jenkins, Docker Hub, SSH  |

---

## 🧰 Prerequisites

Before running or deploying the project, ensure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Jenkins](https://www.jenkins.io/doc/)
- A [Docker Hub](https://hub.docker.com/) account
- A VM (Virtual Machine) with SSH access for deployment

---

## 📦 Getting Started

### 1. **Clone the Repository**

```bash
git clone https://github.com/Sat70/Deployment-Crud-Mean-App.git
cd Deployment-Crud-Mean-App



