# Kubernetes Dashboard with Metrics Server

### Deploy Kubernetes Dashboard using NodePort

```kubectl apply -f dashboard.yaml
```

### Creating A Dashboard user

```kubectl apply -f dashboard-user.yaml
```

### Getting a Token

```kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}" 
```
