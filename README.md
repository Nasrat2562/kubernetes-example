# Kubernetes Aesthetic Dev Workspace

This project demonstrates a modern, aesthetic "Dev Workspace" landing page deployed on a local **Kubernetes** cluster. It showcases container orchestration using **Nginx**, custom HTML/CSS injection, and traffic management through Kubernetes services.

## 🚀 Features
* **Modern UI**: A dark-mode landing page featuring glassmorphism and smooth gradients.
* **Kubernetes Native**: Managed via standard Deployment and Service (LoadBalancer) resources.
* **Lightweight**: Powered by the `nginx:alpine` image for high performance and low footprint.

## 🛠️ Prerequisites
* **Docker Desktop** with **Kubernetes** enabled.
* **kubectl** CLI installed.

## 📁 Required Configuration Files

### 1. Landing Page (`index.html`)
The frontend source code providing the visual interface.

### 2. Deployment Setup (`deployment.yaml`)
Defines the desired state for the application, including container specs and port mapping.

### 3. Service Access (`service.yaml`)
Exposes the application to your local machine using a LoadBalancer.

## 🏃 Setup Instructions

### Step 1: Deploy to Cluster
Run the following commands in your terminal to create the resources:
### step2: Ensure your pod is in the Running state before proceeding:
###Step 3: Access the Application
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl get pods
kubectl port-forward service/my-app-service 8080:80
Visit http://localhost:8080
