# GitOps

## Learn Terraform Provision EKS Cluster

```bash
terraform apply
```

```bash
aws eks --region $(terraform output -raw region) update-kubeconfig \
    --name $(terraform output -raw cluster_name)
```

```bash
kubectl cluster-info
```

```bash
kubectl get nodes
```

## Learn Terraform Helm

Navigate to your [Slack bot services](https://my.slack.com/services/new/bot) and
choose your intended workspace.

Name your app `kubewatch-bot`.

Invite the bot to your channel with the `/invite @kubewatch-bot` command in your
intended Slack channel.

```bash
export TF_VAR_slack_app_token="<YOUR_SLACK_TOKEN>"
```

```bash
terraform apply
```
