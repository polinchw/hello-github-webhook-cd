# hello-github-webhook-cd

## Description

This project contains a Helm chart for Argo CD to deploy [hello-github-webhook](https://github.com/polinchw/hello-github-webhook) to Kubernetes.

## Install ArgoCD Image updater:

```
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj-labs/argocd-image-updater/stable/manifests/install.yaml
```

## Add GitHub token

```
kubectl -n argocd create secret generic git-creds --from-literal=username=polinchw --from-literal=password=xxx
```

### ArgoCD Image Updater Video
[https://www.youtube.com/watch?v=avPUQin9kzU](https://www.youtube.com/watch?v=avPUQin9kzU)

### Instructions

+ Install the ArgoCD Image Updater.
+ Install the secret.
+ Branch this project for dev-# version you want to test with.
+ Deploy the application with:
```
kubectl apply -f application.yaml
```

