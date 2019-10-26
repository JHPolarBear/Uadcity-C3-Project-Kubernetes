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

###Result

- Status
![Alt text](Screenshots/kubectl_status.PNG?raw=true "kubernetes status")

- Pods detail
![Alt text](Screenshots/kubectl_pods.PNG?raw=true "kubernetes pods")


## Local Test

Use port-forward method.

```

# reverseproxy port-foward
kubectl port-forward pod/reverseproxy-85d464d759-tzmgw 8080:8080

# frontend port-foward
kubectl port-forward pod/frontend-778479dfd5-p8zf5 8100:8100

```

###Result

- Application page
![Alt text](Screenshots/app_page.PNG?raw=true "Application page")


