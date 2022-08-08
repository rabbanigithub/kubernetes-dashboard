# Kubernetes Dashboard with Metrics Server

### Deploy Kubernetes Dashboard using NodePort
```
kubectl apply -f dashboard.yaml
```

### Creating A Dashboard user
```
kubectl apply -f dashboard-user.yaml
```

### Getting a Token
```
kubectl -n kubernetes-dashboard create token admin-user
```

### Deploy Metrics Server
```
kubectl apply -f metrics-server.yaml
```

_Disable certificate validation by passing --kubelet-insecure-tls to Metrics Server if Kubelet certificate is not signed cluster Certificate Authority_
