
# Python Flask Docker Application 🐍🐳

A simple Flask application containerized using Docker. This project demonstrates how to create a lightweight Python Docker image and run a Flask application inside a container.

## 📁 Project Structure

```text
project/
│
├── app.py
├── Dockerfile
└── README.md
```

## 🐳 Dockerfile

```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY . .

RUN pip install flask

CMD ["python", "app.py"]
```

## 🛠️ Technologies Used

- Python 3.9
- Flask
- Docker
- Dockerfile

## 🚀 How to Run Locally

### 1. Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <PROJECT_DIRECTORY>
```

### 2. Build Docker Image

```bash
docker build -t flask-app .
```

### 3. Run Docker Container

If your Flask application runs on port `5000`:

```bash
docker run -d -p 5000:5000 --name flask-container flask-app
```

### 4. Check Running Container

```bash
docker ps
```

### 5. Access the Application

Open your browser and visit:

```text
http://localhost:5000
```

## 🔍 Useful Docker Commands

### View Docker Images

```bash
docker images
```

### View Running Containers

```bash
docker ps
```

### View All Containers

```bash
docker ps -a
```

### View Container Logs

```bash
docker logs flask-container
```

### Stop Container

```bash
docker stop flask-container
```

### Remove Container

```bash
docker rm flask-container
```

### Remove Image

```bash
docker rmi flask-app
```

## 📌 Docker Workflow

```text
Flask Application
       ↓
    Dockerfile
       ↓
  docker build
       ↓
   Docker Image
       ↓
    docker run
       ↓
 Docker Container
       ↓
 Flask Application
```

## 🎯 Purpose

This project is created to understand the fundamentals of:

- Dockerfile creation
- Docker image building
- Docker container management
- Flask application containerization
- Port mapping
- Basic Docker commands

## 👨‍💻 Author

**Ritish Chauhan**

B.Tech – Information Technology  
DevOps / Cloud Enthusiast
