# eksctl-automator

Bootstrap a Generally Acceptable EKS Cluster (Kubernetes on AWS)

## REQUIREMENTS

```bash
brew install aws-cli && brew install aws-iam-authenticator
```

## DEPLOYMENT

Create cluster with a template:

```bash
eksctl create cluster -f templates/standard.yaml --profile "${PROFILE}"
````

Delete cluster with a template:

```bash
eksctl delete cluster -f templates/standard.yaml --profile "${PROFILE}"
```

## CONFIGURATION

List available clusters:

```bash
eksctl get clusters --profile "${PROFILE}"
```

Chose cluster you'd like to get credentials for:

```bash
aws eks update-kubeconfig --name "${CLUSTER_NAME} --profile "${PROFILE}""
```

<!-- TODO: Install Autoscaller: -->

<!-- TODO: Install AWS Load Balancer: -->

<!-- TODO: Install Metrics: -->
