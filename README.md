# Using Kubernetes to deploy a simple microservice architecture
This project is based on the course resources offered by https://kodekloud.com/

## Objective
This project grew my infrastructure and automation skills, as I utilized Kubernetes to deploy a microservice architecture solution.

In this project I created deployment files, create ClusterIP services to connect pods to other pods in the cluster, and NodePort services to expose web applications to external users.

The diagram below illustrates the architecture for this solution.

![Terraform drawio](https://github.com/user-attachments/assets/0f8d6f4e-f6b1-4f14-8433-5b36d4f68952)


### Skills Learned

- Kubernetes/kubectl
- yaml

### Tools Used

- Kubernetes
- Visual Studio Code

### Prerequisites 
- Docker
- Kubernetes
- Code/text editor

## Steps to run the solution

### Step 1 - Run the deployment and service files
```
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
```

### Step 2 - Open to the voting app
In your URL navigate to your node ip address and port 30004 to cast you vote
![image](https://github.com/user-attachments/assets/ca900814-c7a9-4a20-aa14-29e4db696d7b)

### Step 2 - Open to the results app
In your URL navigate to your node ip address and port 30005 to view the results
![image](https://github.com/user-attachments/assets/003f58a9-f14f-47f8-8ed6-bd825b16132a)

  
  
  # BasicVotingApp

Create voting app pod and service
![image](https://github.com/user-attachments/assets/1539f883-d1ae-4bd6-9976-d1b35ebd2509)

Voting app can be accessed on local ip and node port
![image](https://github.com/user-attachments/assets/f7c89853-fc24-4ead-9617-395321065438)

