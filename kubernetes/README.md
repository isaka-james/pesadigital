**NOTE:** The Kubernetes specification mentioned here has not been tested avidly and is a community supported definition. I (author) may disregard issues associated with the Kubernetes spec (until I personally shift my homelab to a cluster). 

Use the following instructions to apply the Kubernetes spec:

```bash
kubectl apply -f kubernetes/_namespace.yml
kubectl apply -f kubernetes/Pesadigital-Deployment.yml
kubectl apply -f kubernetes/Pesadigital-configmap.yml
kubectl apply -f kubernetes/Pesadigital-svc.yml
kubectl apply -f kubernetes/Pesadigital-pvc.yml
kubectl apply -f kubernetes/Pesadigital-ingress.yml
kubectl port-forward pod/<pod-name> 8080:8080 # Change Pod Name Here
```

```
Dashboard available at http://pesadigital.localhost/
```
