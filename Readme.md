# Homelab setup with argocd

## Prerequisites

- helm

## Installing argocd

```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

Adding ingress assuming you have nginx

```bash
kubectl apply -f argo/ingress.yaml
```
