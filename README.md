﻿# BasicVotingApp

Create voting app pod and service
![image](https://github.com/user-attachments/assets/1539f883-d1ae-4bd6-9976-d1b35ebd2509)

Voting app can be accessed on local ip and node port
![image](https://github.com/user-attachments/assets/f7c89853-fc24-4ead-9617-395321065438)

kubectl create -f .\voting-app-deploy.yaml
kubectl create -f .\voting-app-service.yaml
kubectl create -f .\redis-deploy.yaml
kubectl create -f .\redis-service.yaml
kubectl create -f .\postgres-deploy.yaml
kubectl create -f .\postgres-service.yaml
kubectl create -f .\worker-app-deploy.yaml 
kubectl create -f .\result-app-deploy.yaml
kubectl create -f .\result-app-service.yaml
kubectl get deployments,svc 


vote app
![image](https://github.com/user-attachments/assets/ca900814-c7a9-4a20-aa14-29e4db696d7b)

result app
![image](https://github.com/user-attachments/assets/003f58a9-f14f-47f8-8ed6-bd825b16132a)
