# 🐍 Flask Notes App with Docker & GitHub Actions

This is a simple Flask web application that allows users to:

- Sign in with a username and password
- Add and delete text notes
- Upload and manage images
- View user-specific content privately

The app is containerized with Docker and automatically built and pushed to Docker Hub using GitHub Actions.

---

## 📦 Features

- 🔐 User Authentication (Session-based)
- 📝 Personal Note Taking
- 🖼️ Image Upload & Management
- 💾 SQLite Database (3 separate DBs for users, notes, images)
- 📄 HTML Templates with Jinja2
- 🐳 Dockerfile for easy containerization
- ⚙️ CI/CD with GitHub Actions and DockerHub Integration

---

## 🚀 Getting Started

### Prerequisites

- Python 3.11+
- Docker installed
- Docker Hub account (for CI/CD)

---

### 🧪 Run Locally (Without Docker)

# Install dependencies
```bash
pip install -r requirements.txt
```

# Run the app
```bash
python app.py
```
# Open your browser and go to:
http://localhost:5000

---

# 🐳 Run with Docker
### Build the Docker image
docker build -t flask-notes-app .

### Run the container
docker run -p 5000:5000 flask-notes-app
Then open:
http://localhost:5000

---

# 🛠️ CI/CD with GitHub Actions
This project includes a GitHub Actions workflow that:

Builds the Docker image on each push to main

Pushes the image to your Docker Hub repository

Make sure to set the following secrets in your GitHub repo:

DOCKERHUB_USERNAME

DOCKERHUB_TOKEN
