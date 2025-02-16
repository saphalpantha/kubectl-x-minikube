# Kubectlxminikube

In Kubernetes World by deploying a Docker image on a local Kubernetes cluster.

## Overview
- Get a hosted Docker image from Docker Hub and run it on a local Kubernetes cluster.
- Access Pods using `kubectl`.
- Control nodes using Minikube.

## Step-by-Step Guide

### 1. Creating a Pod
- Define a pod using `one-pod.yml`.
- Deploy the pod to the Kubernetes cluster.

### 2. Creating a Network
- Use the Kubernetes `Service` object type to create a network.

### 3. Exposing Ports
- Expose the Pod and Node to the outside world.

### 4. Adding a Config File
- Create a configuration file.
- Feed the configuration through `kubectl-api-server`.

### 5. Managing Pods
- Use `kubectl` to manage and control the deployed pods.

### 6. Accessing Deployment
- Use `ClusterIP` and `NodePort` to access the deployment.

## Conclusion
That's it! This project provides a hands-on approach to learning Kubernetes by deploying and managing pods, services, and configurations.

---

### Commands Reference

```sh

# Starting Minikube
minikube start

# Apply the pod definition
kubectl apply -f serve-pod.yml

# Apply the service definition
kubectl apply -f serve-service.yml

# List all pods
kubectl get pods

# Describe a specific pod
kubectl describe pod <pod-name>

# Expose the pod to the outside world
kubectl expose pod <pod-name> --type=NodePort --port=80

# Get the Minikube service URL
minikube service <service-name> --url

# Imperative Update for Deployment with Latest Docker Build

kubectl set image deployment/serve-deployment node=saphalpantha/serve-node:v2

```


Happy Learning! 🚀


#