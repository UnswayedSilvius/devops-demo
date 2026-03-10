# DevOps CI/CD Pipeline Demo

A simple DevOps project demonstrating **Docker containerization, GitHub Actions CI, and Kubernetes deployment**.

## Tech Stack

* Python (Flask)
* Docker
* GitHub Actions
* Kubernetes (Minikube)

## DevOps Workflow

```
Code → GitHub → GitHub Actions CI
        ↓
   Docker Image Build
        ↓
   Kubernetes Deployment
        ↓
   Kubernetes Service
        ↓
   Application Access
```

## Run Locally

Build Docker image:

```
docker build -t devops-demo .
```

Run container:

```
docker run -p 5000:5000 devops-demo
```

Open in browser:

```
http://localhost:5000
```

## Kubernetes Deployment

Start cluster:

```
minikube start
```

Deploy application:

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Access the service:

```
minikube service devops-service
```

## CI Pipeline

A **GitHub Actions workflow** automatically builds and tests the Docker container whenever code is pushed to the `main` branch.


