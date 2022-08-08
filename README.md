# Install Minikube(On MacOS)
brew update
brew install hyperkit
brew install minikube

# Create and Start the Minikube Cluster
minikube start --vm-driver=hyperkit

# Get status of nodes
kubectl get nodes

# Create blue-app
kubectl create -f blue-app.yaml

# Create green-app
kubectl create -f blue-app.yaml

# Checking whether blue-app and green-app is working fine
since Kubernetes v1.10 kubectl port-forward allows using resource name, such as a service name, to select a matching pod to port forward With this connection in place you can use your local workstation to debug the application that is running in the pod.
let's say we got PORT NUMBER 8080
kubectl port-forward [YOUR_PODE_NAME] 8080:8080

# install nginx ingress controller
https://docs.nginx.com/nginx-ingress-controller/installation/installation-with-manifests/

# Create nginx ingress controller
kubectl create -f blue-green-ingress-two.yaml