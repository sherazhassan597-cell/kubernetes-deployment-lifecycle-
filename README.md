# kubernetes-deployment# Commands Used
See commands.txt for full-lifecycle
This project demonstrates a complete Kubernetes deployment lifeKubernetes Deployment Lifecycle
deploy → expose → upgrade → rollback
# Project Overview
In this lab, I practiced core Kubernetes operational tasks using an Nginx application.
# What I Did
 Created an Nginx deployment using kubectl  
 Exposed the deployment using NodePort service  
 Upgraded the container image version  
 Verified rollout status and deployment history  
 Rolled back to the previous stable version 
 # Files in This Repository
 commands.txt  kubectl commands
 # Commands Used
 ```bash
 # Create deployment
  kubectl create deployment nginx --image=nginx:1.14.1 
# Expose deployment 
  kubectl expose deployment nginx --port=80 --target-port=80 --type="NodePort"
# Set image deployment 
  kubectl set image deployment/nginx nginx=nginx=1.16.1 
# Rollback to the previous image 
  kubectl rollout undo deployment/nginx
```
