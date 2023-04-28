This article will show you how to deploy a MySQL database instance on Kubernetes. This feature enables stateful apps to overcome the inherent transience of the K8s pods.

-->Prerequisites
A Kubernetes cluster with kubectl installed
Administrative access to your system

-->MySQL Deployment on Kubernetes
To successfully deploy a MySQL instance on Kubernetes, create a series of YAML files that you will use to define the following Kubernetes objects:
1.A Kubernetes secret for storing the database password.
2.The deployment itself.
3.The Kubernetes Service.

Commands in series:
kubectl apply -f mysql-deployment.yaml
kubectl apply -f mysql-service.yaml
kubectl apply -f mysql-secret.yaml
-->Get a shell for the pod by executing the following command:->
kubectl exec --stdin --tty mysql-694d95668d-w7lv5 -- /bin/bash
-->Type the following command to access the MySQL shell:->
mysql -p

