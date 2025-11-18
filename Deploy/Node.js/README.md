🚀 Kubernetes – Node.js Deployment Guide

This guide explains how to deploy a Node.js application on Kubernetes using YAML manifests for Namespace, Deployment, Service, and an optional standalone Pod.

📁 Project Structure
.
├── nodejs-namespace.yml
├── nodejs-deployment.yml
├── nodejs-service.yml
└── nodejs-pod.yml   (optional)

🏷 1. Create Namespace

Namespaces help organize apps in Kubernetes.

kubectl apply -f nodejs-namespace.yml
kubectl get ns

🚀 2. Deploy Node.js Application
kubectl apply -f nodejs-deployment.yml
kubectl get deployments -n node-js
kubectl get pods -n node-js

🌐 3. Expose Node.js Service
kubectl apply -f nodejs-service.yml
kubectl get svc -n node-js

🧪 4. Optional – Standalone Pod
kubectl apply -f nodejs-pod.yml
kubectl get pods -n node-js
