Installing ArgoCD

https://argo-cd.readthedocs.io/en/stable/getting_started/

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

Excess UI:

```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

username: admin
password: `argocd admin initial-password -n argocd`

To setup argo application.yaml

```bash
kubectl apply -f application.yaml
```

# Deploying datascience etl via argo cd

```bash
kubectl apply -f applications/ftmlAPI.yaml
kubectl apply -f applications/datascienceETL.yaml
```
