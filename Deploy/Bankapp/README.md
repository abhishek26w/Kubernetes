🛠 Step 1: Create a Secure Namespace
Namespaces isolate applications in Kubernetes, like a separate branch of a bank.

    Apply: kubectl apply -f namespace.yml

💾 Step 2: Prepare Storage for Financial Data
Banking data must survive restarts and crashes. We use:

StorageClass – defines how storage is provided
PersistentVolume (PV) – ensures transaction logs aren’t lost

    Create StorageClass: kubectl apply -f manual-sc.yml

💾 Step 3: Set Up Persistent Storage
Create PV and PVC for MySQL.
    
    kubectl apply -f pv.yaml
    kubectl apply -f pvc.yaml

🔐 Step 4: Secure Sensitive Information with Secrets
Passwords must never be exposed in plain text. Kubernetes Secrets encrypt them.

    kubectl apply -f secret.yml

⚙ Step 5: Configure Database with ConfigMaps
Configurations should remain separate from code.

    Apply: kubectl apply -f configmap.yml

🏗 Step 6: Deploy MySQL with StatefulSet with Service
Databases require stable identities and persistent storage.

    Apply: kubectl apply -f mysql-statefulset.yml
           kubectl apply -f mysql-service.yml

💳 Step 7: Deploy the Bank Application

    Apply: kubectl apply -f deployment.yml

🌍 Step 8: Expose the Application

    Apply: kubectl apply -f bankapp-service.yml

🧪 Step 9: Verification Commands

Check everything is running:

    Apply: kubectl get all -n bankapp-namespace

Check logs of your app:

    Apply: kubectl logs -f deployment/bankapp-deployment -n bankapp-namespace

Port forward to access in browser:
    Apply: kubectl port-forward service/bankapp-service -n bankapp-namespace 8080:8080







