```
1. wsl >> windows sublinux 

powershell >> run as admin >> wsl --install 

vtx support should be enable from BIOS

2. powershell >> run as admin >> install chocolately 

3. install docker desktop / website 

4. powershell >> run as admin | minikube install  


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


kubectl delete pods/deployments/services

kubectl delete deployments --all

kubectl delete deployment deploymenty-id

```

