# Using Kubernetes to deploy a microservice solution
This project is based on the course resources offered by https://kodekloud.com/

## Objective
This project grew my infrastructure and automation skills, as I utilized Kubernetes to deploy a microservice architecture solution.

In this project I created kubernetes deployment files, created services to enable network connectivity of pods in my cluster to internal pods and external users.

In this project I:
1. Created a kubernetes deployment file to deploy a web based voting application to cast votes
2. Created a NodePort service to expose the web based voting application to external users
3. Created a kubernetes deployment file to deploy redis to capture the votes on the web based voting application
4. Created a ClusterIP service to enable pods in my cluster to connect to redis
5. Created a kubernetes deployment file to deploy a postgres db to store the vote results
6. Created a ClusterIP service to enable pods in my cluster to connect to postgres
7. Created a kubernetes deployment file to deploy a worker based on .Net to update vote results from redis to postgres
8. Created a kubernetes deployment file to deploy a web based vote result application to view vote results
9. Created a NodePort service to expose the web based result application to external users

The diagram below illustrates the architecture for this solution.

![image](https://github.com/user-attachments/assets/419bbe27-c9b9-40d4-ad1a-141a83f8e91b)



### Skills Learned

- Kubernetes pods
- Kubernetes services (Cluster and NodePort)
- Kubernetes networking
- Kubernetes deployments
- Kubernetes scaling
- yaml
- kubectl

### Tools Used

- Kubernetes/kubectl
- Visual Studio Code

### Prerequisites 
- Docker
- Kubernetes
- Code/text editor

## Steps to create the solution yourself
High level:
1. Create deployment files
   - Voting App
   - Result App
   - Redis
   - Postgres
   - Worker
2. Create Cluster IP Services
   - Redis
   - Postgres
3. Create NodePort Services
   - Voting App
   - Result App

## Steps to run the solution
### Step 1 - Clone and run the deployment/service files
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
```

### Step 2 - Validate deployments and services are running in Kubernetes
```
kubectl get deployments,svc 
```
![image](https://github.com/user-attachments/assets/2ab79096-58e3-4ab4-b0a8-ce7a555bd69f)


### Step 3 - Open to the voting app
In your URL navigate to your node ip address and port 30004 to cast you vote
![image](https://github.com/user-attachments/assets/ca900814-c7a9-4a20-aa14-29e4db696d7b)

### Step 4 - Open to the results app
In your URL navigate to your node ip address and port 30005 to view the results
![image](https://github.com/user-attachments/assets/003f58a9-f14f-47f8-8ed6-bd825b16132a)

