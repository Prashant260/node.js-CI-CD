# Node.js Application with Docker CI/CD

This project is a simple **Node.js** application configured with **Docker** and automated **CI/CD using GitHub Actions**. It is part of the internship tasks for Elevate Labs.

## 📁 Project Structure

Elevate_labs_internship/ ├── .github/ │ └── workflows/ │ └── main.yml # GitHub Actions workflow file ├── nodejsApp/ │ ├── Dockerfile # Dockerfile for Node.js app │ ├── index.js # Main server file │ ├── package.json # App metadata and dependencies │ └── ... # Other app files

yaml
Copy
Edit

---

## 🚀 Features

- Node.js web app
- Dockerized for easy deployment
- GitHub Actions for automated build and push to Docker Hub
- Environment variables managed via GitHub Secrets

---

## 🖥️ Run Locally

### Prerequisites

- Node.js and npm
- Docker (for containerization)

### Steps

1. Clone the repo:
   ```bash
   git clone https://github.com/Prashant260/Elevate_labs_internship.git
   cd Elevate_labs_internship/nodejsApp
Install dependencies:

bash
Copy
Edit
npm install
Start the app:

bash
Copy
Edit
npm start
🐳 Docker Setup
Build Docker Image
bash
Copy
Edit
docker build -t yourusername/nodejsapp:latest .
Run Docker Container
bash
Copy
Edit
docker run -p 3000:3000 yourusername/nodejsapp:latest
The app will be available at http://localhost:3000.

🔁 GitHub Actions CI/CD
Trigger
The workflow is triggered on every push to the main branch.

Actions Workflow
Checkout Code

Log in to Docker Hub (uses secrets)

Build Docker image

Push to Docker Hub

Workflow File: .github/workflows/main.yml

🔐 Secrets Setup
You need to add the following repository secrets in GitHub:

DOCKER_USERNAME → Your Docker Hub username

DOCKER_PASSWORD → Your Docker Hub password or access token

🧑‍💻 Author
Prashant Choudhary
