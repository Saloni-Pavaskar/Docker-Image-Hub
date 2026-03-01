## This project shows how to work with github action

# Docker Image Hub - Flask Application
This project demonstrates how to:
- Containerize a Python Flask application using Docker
- Build and push a Docker image to Docker Hub
- Automate the process using GitHub Actions (CI/CD)

## Tech Stack
- Python 3.9
- Flask
- Docker
- GitHub Actions
- Docker Hub

## Project Structure
Docker-Image-Hub/
│
├── app.py
├── Dockerfile
├── requirements.txt
└── .github/
└── workflows/
└── main.yml

## Dockerfile Overview
- Uses official Python 3.9 slim image
- Sets working directory to `/app`
- Copies project files
- Installs Flask
- Exposes port 5000
- Runs `app.py`

## Build Docker Image (Locally)
```bash
docker build -t salonipavaskar/docker-image-hub:latest .

## Run Docker Container
docker run -p 5000:5000 salonipavaskar/docker-image-hub:latest
Open in browser:
http://localhost:5000
