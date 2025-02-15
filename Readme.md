# Homelab setup with argocd

## Prerequisites

- helm

## Installing argocd

I am installing argo by argocd-autopilot

# Port forward
```
kubectl port-forward -n argocd svc/argocd-server 8080:80
```
