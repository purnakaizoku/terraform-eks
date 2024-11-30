# terraform-eks
Creating an EKS (Elastic Kubernetes Service) cluster using Terraform involves several steps, including defining the necessary resources for EKS and its supporting infrastructure. Here's a step-by-step guide:
1. Prerequisites
Install Terraform: Download and install Terraform.
AWS CLI: Install and configure the AWS CLI with appropriate credentials.
IAM Permissions: Ensure your AWS account has permissions to create EKS clusters and associated resources.
Kubectl: Install kubectl to interact with the Kubernetes cluster.
dairectory structure
eks-terraform/
├── main.tf
├── variables.tf
├── outputs.tf
