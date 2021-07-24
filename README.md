# eksctl-automator

Bootstrap a Generally Acceptable EKS Cluster (Kubernetes on AWS)

## Prerequisites

```bash
brew install aws-iam-authenticator
```

## Deployment

Create cluster with a template:

```bash
eksctl create cluster -f templates/standard.yaml --profile "${PROFILE}"
````

Delete cluster with a template:

```bash
eksctl delete cluster -f templates/standard.yaml --profile "${PROFILE}"
```

## Configuration

```bash
eksctl get clusters --profile "${PROFILE}"
```

```bash
aws eks update-kubeconfig --name "${CLUSTER_NAME} --profile "${PROFILE}""
```
