This note are steps for setting up a k8 cluster with  ansible 

1.Make an entry for the hosts in /etc/hosts file  for the name resolution 
2.Makesure the  k8 master node and worker node are reachable between each other and internet is enabled on both nodes 
3.clone this repository into the master node
4.Get into the directory
cd Task/k8_cluster 
5. There is a file "hosts" available in "k8_cluster" directory, Just make your entries of your all kubernetes nodes
6.Edit your server details in "env_variables" available in "k8_cluster" directory.
7.Deploy the ssh key from master node to other nodes for password less authentication.

ssh-keygen

Copy the public key to the worker nodes including  the  master node and make sure you are able to login into any nodes without password.
8.Run "settingup_kubernetes_cluster.yml" playbook to setup all nodes and kubernetes master configuration.

ansible-playbook settingup_kubernetes_cluster.yml

9.Run "join_kubernetes_workers_nodes.yml" playbook to join the worker nodes with kubernetes master node once "settingup_kubernetes_cluster.yml" playbook tasks are completed.

ansible-playbook join_kubernetes_workers_nodes.yml

10.Verify the configuration from master node.

kubectl get nodes




