# DevOps FastAPI Assignment

## Overview
This project demonstrates deployment of a FastAPI application using Docker, Docker Compose, Nginx, PostgreSQL, Redis, and GitHub Actions.

## Architecture

Internet
   |
 Nginx
   |
 FastAPI
 /      \
Redis  PostgreSQL

## Technologies Used

- FastAPI
- Docker
- Docker Compose
- Nginx
- PostgreSQL
- Redis
- GitHub Actions

## Setup

### Clone Repository

git clone <repo-url>

### Run Application

docker compose up -d

### Check Running Containers

docker ps

## Health Endpoint

http://localhost:8000/health

## CI/CD

GitHub Actions automatically builds the Docker image on every push to main.

## Security Measures

- Environment variables
- Nginx reverse proxy
- Containerized deployment

## Backup Strategy

PostgreSQL backup:

docker exec postgres pg_dump -U admin appdb > backup.sql

## Future Improvements

- SSL using Let's Encrypt
- Monitoring using Prometheus and Grafana
- Automated deployment to AWS EC2
