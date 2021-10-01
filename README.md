# Task to setpup a Kubernetes cluster using ansible and  deploy a test image 
Related questions on task to be carried out can be found in notes.txt
There are two parts to the questions ;
 i. Setting up of a kubernetes cluster   --- Task/k8_cluster, there is a readme.txt to follow in the folder 
 ii. writing a yaml script for deployment ,service , Persistent volume, Persistent Volume Claim   ---Task/k8s_deployments
To  the k8s_deployments scripts follow the steps below;
a. clone the file Task/k8s_deployments
b. cd to your file path and run kubectl create -f k8s_deployments.yaml
c. once this is  done comfirm that all objects has been created and are running . to confirm that you can run "kubectl get all"
d. once they are running , attemp to access the  the deployed  image from your browser "clusterIP:31000{or value in nodeport}"
e. If you encouner any error accessing it kindly check the firewall rule on your cluster to permit that port.

Happy coding !!!
