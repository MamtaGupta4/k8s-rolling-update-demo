# 🚀 Kubernetes Rolling Update & Rollback Demo

This project demonstrates Kubernetes rolling updates and rollback functionality using an Nginx application deployed with a Deployment.

## 🛠 Technologies Used

- Kubernetes
- Minikube
- Docker
- Nginx
- kubectl

## 📂 Project Structure

```text
k8s-rolling-update-demo/
│
├── Dockerfile
├── deployment.yaml
├── service.yaml
├── index.html
└── README.md
```

## 🚀 Deployment

Apply Kubernetes resources:

```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

Check deployment and pods:

```bash
kubectl get deployments
kubectl get pods
```

## 🔄 Rolling Update

Build a new image version and update the deployment:

```bash
kubectl set image deployment/rolling-update-demo \
webapp=rolling-update-demo:v2
```

Check rollout status:

```bash
kubectl rollout status deployment/rolling-update-demo
```

## 🔙 Rollback

View rollout history:

```bash
kubectl rollout history deployment/rolling-update-demo
```

Rollback to the previous version:

```bash
kubectl rollout undo deployment/rolling-update-demo
```

## 🎯 Concepts Covered

- Deployments
- ReplicaSets
- Services
- Rolling Updates
- Rollback
- Container Versioning

## ✅ Result

Successfully demonstrated application updates and rollback in Kubernetes using an Nginx-based deployment.
