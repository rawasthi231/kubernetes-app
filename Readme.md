# Deploy MERN app (MongoDB) with Kubernetes

### Install kubectl

[Checkout the installation guide](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/)

### Install minikube

[Checkout the installation guide](https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download)

### Commands

- Start minicube and run docker containers after downloading the required docker images
  ```cmd
  minikube start
  ```
- Get all the deployed pods
  ```cmd
  kubectl get pods
  ```
- Get all the running services
  ```cmd
  kubectl get svc
  ```
- Remove all the deployed pods
  ```cmd
  kubectl remove deployments --all
  ```
- Remove all the running services
  ```cmd
  kubectl delete service --all
  ```
- Remove all the created secrets
  ```cmd
  kubectl delete secret --all
  ```
- Remove all the created configMaps
  ```cmd
  kubectl delete configmap --all
  ```
- Apply the YAML file to create secrets. Simillarily you can it for pods, services and configMaps
  ```cmd
  kubectl apply -f .\secrets.yaml
  ```
- Get minikube informations
  ```cmd
  kubectl get node -o wide
  ```
- Get the minikube IP
  ```cmd
  minukube ip
  ```
- Map the running webapp-service with the minikube in order to run on local machine
  ```cmd
  minikube service webapp-service
  ```
