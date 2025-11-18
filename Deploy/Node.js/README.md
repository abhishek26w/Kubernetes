1. Create Namespace
kubectl apply -f nodejs-namespace.yml
kubectl get ns

2. Deploy Node.js Application
kubectl apply -f nodejs-deployment.yml
kubectl get deployments -n node-js
kubectl get pods -n node-js

3. Expose Node.js Service
kubectl apply -f nodejs-service.yml
kubectl get svc -n node-js

4. Optional – Standalone Pod
kubectl apply -f nodejs-pod.yml
kubectl get pods -n node-js

