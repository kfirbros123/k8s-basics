# kfirs-app-k8s

Apply these manifests in this order:

```bash
kubectl apply -f configmap.yaml
kubectl apply -f secret.example.yaml
kubectl apply -f postgres-pvc.yaml
kubectl apply -f postgres-deployment.yaml
kubectl apply -f postgres-service.yaml
kubectl apply -f kfirs-app-deployment.yaml
kubectl apply -f kfirs-app-service.yaml
```

Local access (no Ingress included):

```bash
kubectl port-forward svc/kfirs-app 8080:8080
```

