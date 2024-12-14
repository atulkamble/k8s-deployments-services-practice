git clone https://github.com/atulkamble/k8s-deployments-services-practice.git
kubectl apply -f deployment.yaml 
kubectl get deployments
kubectl apply -f deployment.yaml 
sudo nano deployment.yaml 
kubectl apply -f deployment.yaml 
 

Attach Policy for EKSClusterRole


AmazonEKSBlockStoragePolicy
AmazonEKSComputePolicy
AmazonEKSLoadBalancingPolicy
AmazonEKSNetworkingPolicy

NodeGroupRoles
EC2 

{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Effect": "Allow",
			"Principal": {
				"Service": "eks.amazonaws.com"
			},
			"Action": [
				"sts:AssumeRole",
				"sts:TagSession"
			]
		}
	]
}




