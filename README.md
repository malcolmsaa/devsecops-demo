# DevSecOps Demo

## Stack
- Python (Flask)
- Docker
- Kubernetes

## Run locally

docker build -t devsecops-demo:latest .
docker run -p 5000:5000 devsecops-demo

## Kubernetes

kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml

kubectl port-forward service/devsecops-demo-service 8080:80

Open:
http://localhost:8080

## Scale

kubectl scale deployment devsecops-demo --replicas=2

## Logs

kubectl logs deployment/devsecops-demo
