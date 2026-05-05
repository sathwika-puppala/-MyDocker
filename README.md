# Dockerized Hello World Application

## Overview
This project demonstrates a simple Flask-based web application containerized using Docker. The app serves a basic "Hello World" message and is accessible over a local network (intranet).

---

## Tech Stack
- Python 3
- Flask
- Docker

---

## Project Structure
.
├── app.py
├── requirements.txt
└── Dockerfile

---

## Application Behavior
- Runs on port 5000
- Returns "Hello World from Docker!" when accessed

---

## Build Docker Image
Run inside the project folder:
docker build -t hello-docker-app .

---

## Run Docker Container
docker run -d -p 5000:5000 hello-docker-app

---

## Access the Application

### On same system
http://localhost:5000

### On another device (same Wi-Fi)
http://172.16.1.227:5000

---

## Intranet Communication
The app runs on host 0.0.0.0, which allows it to be accessed by other devices in the same network using your IPv4 address.

---

## Verification Steps
1. Check running containers:
   docker ps

2. Confirm port mapping:
   0.0.0.0:5000->5000

---

## Notes
- Make sure port 5000 is allowed in firewall
- Both devices should be connected to same network


