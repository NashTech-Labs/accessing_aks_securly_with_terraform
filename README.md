# Azure Infrastructure Deployment using Terraform

This script is use to securely access an AKS cluster via Terraform, establish VNet peering between AKS VNet and VM VNet, configure network security rules, and use kubectl commands from the VM for secure communication.

## Prerequisites

- **Azure Subscription:** Ensure you have an active Azure subscription.
- **Terraform Installed:** Download Terraform from [terraform.io](https://www.terraform.io/downloads.html).

## Deployed Resources

#### AKS Cluster

#### Virtual Network 1

#### Virtual Network 2

#### Linux Virtual Machine

## Usage

1. Clone this repository to your local machine.
2. Navigate to the directory containing the Terraform code.
3. Initialize the Terraform directory using the command `terraform init`.
4. Create an execution plan with `terraform plan`.
5. Apply the plan with `terraform apply`. You will be prompted to confirm the action by typing `yes`.
6. Once the infrastructure is created, you can connect to your EC2 instance.

Remember to run `terraform destroy` when you no longer require these resources to avoid unnecessary AWS charges.
