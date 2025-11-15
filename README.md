# TaskApp

A simple and scalable task management application built with **Node.js**, **Express**, and **Docker**, designed for easy deployment and CI/CD automation using **Jenkins**.

---

## 🚀 Overview

TaskApp is a backend application that allows users to manage tasks through a clean REST API. It's containerized for portability and includes a Jenkins pipeline for automated builds.

### Tech Stack

* **Node.js / Express** – Core API
* **Docker & Docker Compose** – Containerization
* **Jenkins** – CI/CD automation
* **ENV configuration system** – Secure configuration via `.env`

---

## 📁 Project Structure

```
TaskApp/
│
├── config/              # App configuration files
├── src/                 # Application source code (routes, controllers, logic)
│
├── Dockerfile           # Docker image definition
├── docker-compose.yml   # Multi-container setup
├── Jenkinsfile          # CI/CD pipeline
├── .dockerignore        # Files ignored by Docker
├── .env                 # Environment variables (not for production)
│
├── package.json         # Project metadata & dependencies
├── package-lock.json    # Dependency lock file
└── README.md            # Project documentation
```

---

## 🏗️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/TaskApp.git
cd TaskApp
```

### 2️⃣ Install dependencies

```bash
npm install
```

### 3️⃣ Create a `.env` file

Example:

```
PORT=3000
MONGO_URI=mongodb://localhost:27017/taskapp
```

### 4️⃣ Start the app

```bash
npm run start
```

---

## 🐳 Run with Docker

### Build the image

```bash
docker build -t taskapp .
```

### Run the container

```bash
docker run -p 3000:3000 --env-file .env taskapp
```

### Using Docker Compose

```bash
docker compose up --build
```

---

## ⚙️ Jenkins CI/CD Pipeline

The included `Jenkinsfile` automates:

* 🔍 Linting & tests
* 🏗️ Docker build
* 📦 Image push to registry
* 🚀 Deployment (optional)

To use it:

1. Create a Jenkins Pipeline project
2. Point it to this repo
3. Configure Docker & credentials

---

## 📡 API Endpoints

(Example structure — customize based on your routes)

```
GET    /tasks        # Fetch all tasks
POST   /tasks        # Create new task
PUT    /tasks/:id    # Update task
DELETE /tasks/:id    # Delete task
```

---

## 🧪 Testing

Add tests inside the `src/tests` folder (if available):

```bash
npm test
```

---

## 🤝 Contributing

Pull requests, issues, and suggestions are welcome!

---

## 📄 License

Open-source under the MIT License.
