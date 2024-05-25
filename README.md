
# Project Title

A brief description of what this project does and who it's for


## Installation

The YAML file, contains Deploymment to pull weather app from the Private docker hub reposioty. 

Create a secret-file using

```bash
kubectl create secret docker-registry my-registry-secret \
--docker-server=docker.io \
--docker-username=DOCKER_USER \
--docker-password=DOCKER_PASSWORD \
--docker-email=DOCKER_EMAIL
```

Then create the deployment using 
```bash
Kubectl apply -f weather_app_deployment_from_docker_private_repo.yaml
```


In Minikube to expose the service using port forwarding use: 
```bash
kubectl port-forward svc/weather-app-service 3000:3000
```
