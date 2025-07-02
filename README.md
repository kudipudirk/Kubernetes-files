# Kubernetes CLI Setup for Amazon EKS

This guide explains how to set up `kubectl` and `eksctl` to work with Amazon EKS on a Linux system.

---

## ✅ Prerequisites

- AWS account with IAM user/role that has EKS permissions
- AWS CLI configured (`aws configure`)
- `curl`, `tar`, and `jq` installed

---

## 🔧 1. Install eksctl

```bash
curl --silent --location "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
sudo mv /tmp/eksctl /usr/local/bin
eksctl version

## 🔧 1. Install kubectl

curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.33.0/2025-05-01/bin/linux/amd64/kubectl
chmod +x kubectl
sudo mv kubectl /usr/local/bin
kubectl version --client

Note: Update the version as needed: https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html

## 🛠️ 3. Configure AWS CLI
aws configure
Enter:
Access Key ID
Secret Access Key

🚀 4. Create an EKS Cluster

eksctl create cluster -f < file_name >

