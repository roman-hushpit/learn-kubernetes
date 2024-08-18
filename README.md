# learn-kubernetes


# Run Minikube
minikube start --extra-config "apiserver.cors-allowed-origins=["http://boot.dev"]"

# Dashboard
minikube dashboard --port=63840

# Previous minikube installations
minikube stop
minikube delete

# Deploying an image
kubectl create deployment synergychat-web --image=bootdotdev/synergychat-web:latest

# Viewing deployments
To make sure the deployment was successful, run:

kubectl get deployments

# Accessing the web page

kubectl get pods
kubectl get pods -o wide

kubectl port-forward PODNAME 8080:8080

Be sure to replace PODNAME with your pod's name. Example: synergychat-web-679cbcc6cd-cq6vx


# Tips
## If you want to set VS Code as your default text editor, you can add:

export EDITOR="code -w"

to your .zshrc or .bashrc file

# Access pod logs
kubectl logs PODNAME

# Delete pods
kubectl delete pod PODNAME

kubectl apply -f api-deployment.yaml

kubectl get configmaps

kubectl apply -f api-configmap.yaml

# Persistent Volume Claims (PVC)

kubectl get pvc
kubectl get pv
kubectl delete pvc <pvc-name>