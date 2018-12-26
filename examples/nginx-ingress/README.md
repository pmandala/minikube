# Setting Minikube with Ingress Controller

Create a security for the pulling the image from docker hub

```
kubectl create secret docker-registry dockerhub --docker-username= --docker-password=   --docker-email=
```


Setup Nginx Ingress Controller on Minikube

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/mandatory.yaml
minikube addons enable ingress
```


Deploy into minikube

```
kubectl create -f deployment.yaml
kubectl create -f service.yaml
kubectl create -f ingress.yaml
```
