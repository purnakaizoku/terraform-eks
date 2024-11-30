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
3. Initialize and Apply
Initialize Terraform: Run the following command to initialize your Terraform project.

terraform init
Validate the Configuration: Check for errors in the configuration.

terraform validate
Plan the Deployment: Review the changes Terraform will make.

terraform plan
Apply the Configuration: Deploy the EKS cluster.

terraform apply
4. Configure Kubectl
Retrieve the kubeconfig file for the cluster and set it up.

aws eks update-kubeconfig --name my-eks-cluster --region us-east-1
Test connectivity:

kubectl get nodes
5. Clean Up
When you no longer need the cluster, clean up resources by running:

terraform destroy
6. Notes
The Terraform AWS modules used (vpc and eks) simplify the process of creating EKS clusters.
Adjust the cluster version and instance types based on your requirements.
Use a backend (e.g., S3) to store the Terraform state file securely for production setups.
