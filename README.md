Dockerized Hello World Application
Overview
This project demonstrates a minimal web application packaged as a Docker container. The application responds with a simple message and is accessible over a local network (intranet).

Tech Stack
Python 3
Flask
Docker

Project Structure
.
├── app.py
├── requirements.txt
└── Dockerfile

Application Behavior
Runs a Flask server on port 5000
Returns a plain text response when accessing /

Build Instructions
Run the following command in the project directory:
docker build -t hello-docker-app .

Run the Container
docker run -d -p 5000:5000 hello-docker-app

Access the Application
On Local Machine
http://localhost:5000
On Another Device (Same Network)
http://172.16.1.227:5000

Intranet Communication
The application binds to 0.0.0.0, allowing access from other devices within the same network. Using your system’s IPv4 address enables testing across devices.

Verification
Ensure the container is running:
docker ps
Confirm port mapping:
0.0.0.0:5000->5000

Notes
Ensure port 5000 is not blocked by firewall settings
Both devices must be connected to the same network

Repository
Upload this project to your GitHub repository and share the link as required.
