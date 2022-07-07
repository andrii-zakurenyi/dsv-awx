```
minikube start --cpus=4 --memory=6g --addons=ingress
```

```
kubectl apply -k .
```

```
kubectl get pods -n awx
```

```
minikube service awx-demo-service --url -n awx
```

```
kubectl get secret awx-demo-admin-password -n awx -o jsonpath="{.data.password}" | base64 --decode
```