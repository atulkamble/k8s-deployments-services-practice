ec2 - t2.medium - amazon linux - ssh 
```
// EC2 instance type: t2 medium

sudo yum update -y
sudo yum install docker -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER && newgrp docker
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
ls
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube version
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
ls
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
kubectl version --client
minikube start --driver=docker
minikube status
kubectl get nodes
minikube addons enable dashboard
minikube dashboard
minikube stop
minikube delete

// alternatives
minikube dashboard --url

examples:

// URL
http://127.0.0.1:44157/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/

//command
ssh -L 9999:127.0.0.1:44157 -i minikube.pem ec2-user@ec2-184-73-142-125.compute-1.amazonaws.com

// dashboard
http://127.0.0.1:9999/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/
```

