# Kubernetes Deployment Task

## Objective
Deploy and manage an Nginx app in Kubernetes using Minikube.

## Tools Required
- Minikube
- kubectl
- Docker

## Steps

### 1. Install Minikube
Refer to the official documentation: https://minikube.sigs.k8s.io/docs/start/

### 2. Start Minikube
```bash
minikube start
```

### 3. Deploy the Application
Apply the deployment and service YAML files:
```bash
kubectl apply -f deployment.yml
kubectl apply -f service.yml
```

### 4. Verify Pods and Services
```bash
kubectl get pods
kubectl get services
```

### 5. Access the Application
Get the Minikube IP and access the app:
```bash
minikube ip
```
Visit `http://<minikube-ip>:30008` in your browser.

### 6. Scale the Deployment
```bash
kubectl scale deployment myapp-deployment --replicas=4
```

### 7. View Pod Details and Logs
```bash
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

## Deliverables
- `deployment.yml` and `service.yml` files
- Screenshots:
  - Pods (`kubectl get pods`)
  - Services (`kubectl get services`)
  - Nginx page in browser
  - Logs (`kubectl describe pod`)
