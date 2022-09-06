# Kubernetes Microservices Application
Repository for and app (Wordpress + MySQL) with microservices on Kubernetes.

## Prerequisites
1. You have Docker installed on your local machine.
2. You have Kubernetes installed on your local machine or via Docker.


## Setup Steps
1. Clone this repo.
2. In the new project folder, run the following command:
'''sh
kubectl create -f 
'''


## How to access the application?
1. Check the Port created by executing the command:
'''sh
kubectl get svc
'''
2. Use port forwarding to access the application in the Cluster IP:
'''sh
kubectl port-forward deployment/[deploment_name] 8080:80
'''
3. The output is similar to this:
'''
Forwarding from 127.0.0.1:8080 -> 80
Forwarding from [::1]:8080 -> 80
Handling connection for 8080
'''


## Notes:
   - kubectl port-forward does not return. To continue, you will need to open another terminal.
   - kubectl port-forward is implemented for TCP ports only.


Now, you should access Wordpress on port 8080 connected to MySQL.
