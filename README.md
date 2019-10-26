# Udagram Course-3 Project


## Project platform

This project is built and tested with Amazon EKS and CLI


## Docker Container List

Restapi-feed : https://cloud.docker.com/u/jhpark8904/repository/docker/jhpark8904/udacity-restapi-feed

Restapi-users: https://cloud.docker.com/u/jhpark8904/repository/docker/jhpark8904/udacity-restapi-user

frontend: https://cloud.docker.com/u/jhpark8904/repository/docker/jhpark8904/udacity-frontend

Reverseproxy: https://cloud.docker.com/u/jhpark8904/repository/docker/jhpark8904/reverseproxy


## Installation

```

# environment settings
kubectl apply -f env-configmap.yaml
kubectl apply -f env-secret.yaml
kubectl apply -f aws-secret.yaml

# restapi settings
kubectl apply -f backend-user-deployment.yaml
kubectl apply -f backend-feed-deployment.yaml

kubectl apply -f backend-user-service.yaml
kubectl apply -f backend-feed-service.yaml

# frontend and reverseproxy
kubectl apply -f frontend-deployment.yaml
kubectl apply -f reverseproxy-deployment.yaml

kubectl apply -f frontend-service.yaml
kubectl apply -f reverseproxy-service.yaml 	

```