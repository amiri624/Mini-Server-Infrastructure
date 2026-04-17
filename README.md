# Mini-Server-Infrastructure

Markdown
# 🐧 Docker-Based Linux Infrastructure
```bash
<p align="center">
  <img src="https://img.shields.io/badge/Linux-Ubuntu-orange">
  <img src="https://img.shields.io/badge/Docker-Container-blue">
  <img src="https://img.shields.io/badge/Nginx-WebServer-green">
  <img src="https://img.shields.io/badge/MySQL-Database-blue">
</p>

---
```
## 📌 Overview
```bash
This project demonstrates a simple but realistic **container-based infrastructure** using Docker and Docker Compose.

It simulates a production-like environment including:
- Web Server
- Database
- Service orchestration

💡 Built to showcase hands-on skills in **Linux Administration & DevOps fundamentals**

---
```
## 🏗️ Architecture

```bash
    ┌────────────────────┐
    │     Browser        │
    │  http://localhost  │
    └─────────┬──────────┘
              │
              ▼
    ┌────────────────────┐
    │      Nginx         │
    │   (Web Server)     │
    └─────────┬──────────┘
              │
              ▼
    ┌────────────────────┐
    │      MySQL         │
    │    (Database)      │
    └────────────────────┘
```

## ⚙️ Technologies
```bash
- 🐳 Docker & Docker Compose
- 🌐 Nginx
- 🗄️ MySQL
- 🐧 Linux

---
```
## 📁 Project Structure

# my-project/
├── docker-compose.yml
├── README.md

---

## 🚀 Getting Started

### Start the project

```bash
docker-compose up -d
```

## Check running containers

```bash
docker ps
```

# 🌐 Access Web Server → http://localhost:8080
## 🔧 Configuration

```bash
MYSQL_ROOT_PASSWORD=root
```

## Step one

```bash
sudo apt update
sudo apt install docker.io docker-compose -y
```

## Then

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

## Test

```bash
docker run hello-world
```

## Step two

```bash
docker run -d -p 8080:80 nginx
```

# Phase 2

```bash
mkdir my-project
cd my-project
nano docker-compose.yml
```
## Than Content 
```bash
version: '3'

services:
  web:
    image: nginx
    ports:
      - "8080:80"
```
## Execution

```bash
docker-compose up -d
```

# Phase 3: Adding the Database

```bash
version: '3'

services:
  web:
    image: nginx
    ports:
      - "8080:80"

  db:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: root
```

# Phase 5 Backup

```bash
vim backup.sh
```

```bash
#!/bin/bash
tar -czf backup.tar.gz .
```

## Execution

```bash
chmod +x backup.sh
./backup.sh
```



# 📊 Skills Demonstrated
. Linux Server Administration
. Docker Containerization
. Service Deployment
. Infrastructure Setup
. Basic Networking Concepts


# 🔮 Future Improvements

. 📦 Add Docker Volumes (Data Persistence)
. 📊 Monitoring (Prometheus & Grafana)
. 🔁 Backup Automation (Bash Script)
. 🔒 Security Hardening
. ☁️ Cloud Deployment (AWS / Azure)


### 💻 Author

M-A
Linux System Administrator | DevOps Enthusiast

