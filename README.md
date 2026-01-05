\# CI/CD Pipeline (GitHub Actions + Kubernetes)



\## What this project does

This project shows a CI/CD pipeline that builds and validates a containerized app and deploys it to Kubernetes.



\## Tools used

\- GitHub Actions

\- Docker

\- Kubernetes



\## Architecture Diagram



!\[CI/CD Architecture](docs/diagrams/architecture.png)



\## Repo structure

\- .github/workflows/ci.yml  (CI pipeline)

\- app/                      (sample app)

\- k8s/                      (Kubernetes manifests)



\## How to run locally (optional)

1\. Build image:

&nbsp;  docker build -t myapp:local ./app

2\. Run:

&nbsp;  docker run -p 8080:8080 myapp:local



\## Deploy to Kubernetes

1\. Apply manifests:

&nbsp;  kubectl apply -f k8s/

2\. Check resources:

&nbsp;  kubectl get pods

&nbsp;  kubectl get svc



\## CI/CD Workflow (GitHub Actions)

On every push to main:

\- Checkout code

\- Run lint/tests

\- Build Docker image

\- (Optional) Push image

\- Validate Kubernetes manifests



\## Proof / Screenshots

Add screenshots here:

\- GitHub Actions run success

\- kubectl get pods / svc output



\## Troubleshooting

\- If pipeline fails: check Actions logs

\- If pods fail: kubectl describe pod <name> and kubectl logs <pod>



\## What I learned

\- Writing repeatable CI workflows in GitHub Actions

\- Validating deployments before releasing to Kubernetes



