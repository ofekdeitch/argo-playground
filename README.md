Install Argo CD:

```
kubectl create namespace argocd
kubectl apply -n argocd -f argocd/install.yaml
```


Get admin password:

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

Create playground apps

```
kubectl apply -n argocd -f argocd/apps.yaml
```
