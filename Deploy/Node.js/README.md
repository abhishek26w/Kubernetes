🚀 Kubernetes Commands – Node.js Deployment
# 📌 Create Namespace
kubectl apply -f nodejs-namespace.yml
kubectl get ns

# 🚀 Deploy Node.js Application
kubectl apply -f nodejs-deployment.yml
kubectl get deployments -n node-js
kubectl get pods -n node-js

# 🌐 Expose Service
kubectl apply -f nodejs-service.yml
kubectl get svc -n node-js

# 🧪 Optional: Standalone Pod
kubectl apply -f nodejs-pod.yml
kubectl get pods -n node-js
