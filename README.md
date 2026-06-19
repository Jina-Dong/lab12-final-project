# Lab 12 Final Project

## Personal Info
- **Name**: Dong Jinai
- **Student ID**: 20242187
- **Photo**:

  ![my photo](website/images/me.jpg)

## Application URLs
- Personal Website: http://54.242.6.114:7070
- Todo App: http://54.242.6.114:7090

## Tech Stack
- Docker & Dockerfile
- Docker Compose
- GitHub Actions (automated deployment to AWS EC2 via SSH)
- Nginx (for static website hosting)
- Todo App Source Repository: https://github.com/docker/getting-started-app

## Deployment Architecture
This project deploys both the personal static website and Todo application simultaneously on a single AWS EC2 instance using a `docker-compose.yml` configuration file.

A GitHub Actions workflow defined at `.github/workflows/deploy.yml` is triggered automatically whenever new commits are pushed to the main branch. The workflow establishes an SSH connection to the remote EC2 server, then executes the command `docker compose up -d --build` to rebuild container images and restart services for continuous automatic deployment.
