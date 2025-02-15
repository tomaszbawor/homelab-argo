# Homelab setup with argocd

## Prerequisites

- helm

## Installing argocd

I am installing argo by argocd-autopilot


## Recovering From an Existing Repository¶
If, for any reason, something happens to your argo-cd installation, you can recover from an existing repository using the --recover flag.

This should re-apply Argo-CD to the cluster, then create the autopilot-bootstrap application, which will restore all of the other applications in your repository.

```bash
export GIT_REPO=https://github.com/owner/installation-repo
export GIT_TOKEN=xxx

argocd-autopilot repo bootstrap --recover
```

# Port forward
```
kubectl port-forward -n argocd svc/argocd-server 8080:80
```
