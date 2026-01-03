https://github.com/swecha3108/cicd-github-actions-k8s/actions/workflows/ci.yml/badge.svg



\# CI/CD Demo - GitHub Actions + Docker + Kubernetes



\## Description

A small Flask API containerized with Docker and built via GitHub Actions. The workflow builds and pushes the image to GitHub Container Registry (GHCR). Kubernetes manifests are included for deployment.



\## Tools

GitHub Actions, Docker, Kubernetes (YAML), Git/GitHub



\## CI Pipeline

Workflow: `.github/workflows/ci.yml`

\- Triggers on push to `main` and pull requests

\- Builds Docker image and pushes to GHCR as: `ghcr.io/<owner>/<repo>:latest`



\## Kubernetes

Manifests: `k8s/`

\- `deployment.yaml`

\- `service.yaml`



