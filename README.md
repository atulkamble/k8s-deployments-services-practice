# k8s-deployments-services-practice


```
git clone https://github.com/atulkamble/k8s-deployments-services-practice
cd k8s-deployments-services-practice
```

```
Open powershell as admin >> minikube installation

Run Docker desktop in background >> minikube start 


// create file from windows terminal

touch - New-Item 

// open code from windows terminal
code .

code name-of-file.yaml



start single node cluster - 


// installation of minikube 

https://minikube.sigs.k8s.io/docs/start/

// start cluster 

minikube start 

minikube stop 

minikube delete

// troubleshooting 
tip: start docker engine/ docker desktop running 

// project
mkdir k8sproject
cd k8sproject

// create deployment file
touch deployment.yaml

```
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
  labels:
    app: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: my-container
        image: my-image:1.0
        ports:
        - containerPort: 80
```
// check contents of file
cat deployment.yaml

// apply deployment 
kubectl apply -f deployment.yaml

// check deployment
kubectl get deployments

// check pods 
kubectl get pods

// edit file 
sudo nano deployment.yaml

// apply deployment
kubectl apply -f deployment.yaml


// check pods 
kubectl get pods

// check services 
kubectl get services 

// dashboard 
minikube dashboard 

// add plugin 

minikube addons list 

minikube addons enable metrics-server

```
