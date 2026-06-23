# DevOps FastAPI Assignment

## Overview

This project demonstrates deployment of a FastAPI application using Docker, Docker Compose, Nginx, PostgreSQL, Redis, and GitHub Actions.

---

## Architecture

                Internet
                    |
                 Nginx
                    |
                 FastAPI
                /       \
               /         \
          PostgreSQL    Redis

---

## Technologies Used

- FastAPI
- Docker
- Docker Compose
- PostgreSQL
- Redis
- Nginx
- GitHub Actions

---

## Project Structure

devops-fastapi-assignment/

├── app/
│   └── main.py

├── nginx/
│   └── nginx.conf

├── .github/
│   └── workflows/
│       └── deploy.yml

├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── .env
└── README.md

---

## Setup Instructions

### Clone Repository

git clone <repository-url>

### Start Application

docker compose up -d

### Verify Containers

docker ps

---

## Endpoints

Home:

http://localhost

Health Check:

http://localhost:8000/health

---

## CI/CD Pipeline

GitHub Actions automatically builds the Docker image whenever code is pushed to the main branch.

---

## Security Measures

- Environment variables used for configuration
- Nginx reverse proxy
- Docker container isolation
- SSH key authentication for production
- Firewall configuration using UFW

---

## Backup Strategy

Create backup:

docker exec postgres pg_dump -U admin appdb > backup.sql

Restore backup:

cat backup.sql | docker exec -i postgres psql -U admin appdb

---

## SSL Strategy

For production deployment, SSL can be implemented using Let's Encrypt and Certbot.

---

## Deployment

The application has been tested locally using Docker Compose.

For production deployment:

1. Launch an Ubuntu server.
2. Install Docker and Docker Compose.
3. Clone the repository.
4. Run:

docker compose up -d

5. Expose ports 80 and 443.

---

## Future Improvements

- Prometheus Monitoring
- Grafana Dashboards
- Automated AWS Deployment
- SSL Automation
