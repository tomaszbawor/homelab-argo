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

# TODO: 

Currently I do not know how to store sops encrypted JSON files to be interpreted by Argo-CD. Temporary we can add secrets by hand. 

In the future I would like to encrypt them using SOPS

Currently `cloudflare-api-token.yaml` is needed for the SSL cert generation
In order to manually do that you have to decrypt it using sops 

```bash
sops -d cloudflare-api-token.yaml > secret.yaml
kubectl apply -f secret.yaml
```

This will manually put secret into the cluster and enable cert manager to issue a cert request. 
