# Homelab setup with argocd

## Prerequisites

- helm

## Installing argocd

```bash
helm repo add argo https://argoproj.github.io/argo-helm
```

and then 

```bash
helm install argo-cd argo/argo-cd --version 7.8.2
```
