# Azure Infrastructure Deployment using Terraform

This Terraform script automates the deployment of Azure resources, including an AKS cluster, virtual networks, subnets, and a Linux virtual machine. Follow the instructions below to deploy and manage the infrastructure.

## Prerequisites

- **Azure Subscription:** Ensure you have an active Azure subscription.
- **Terraform Installed:** Download Terraform from [terraform.io](https://www.terraform.io/downloads.html).

## Deployed Resources

### AKS Cluster

- **Name:** `my-aks-cluster`
- **Location:** `japan east`
- **Node Pool:**
  - **Name:** `default`
  - **Node Count:** 1
  - **VM Size:** `Standard_DS2_v2`
  - **Auto Scaling:** Enabled (1 to 2 nodes)
  - **Type:** `VirtualMachineScaleSets`

- **Network Profile:**
  - **Network Plugin:** `kubenet`
  - **DNS Service IP:** `192.168.1.1`
  - **Service CIDR:** `192.168.0.0/16`
  - **Pod CIDR:** `172.16.0.0/22`
  - **Private Cluster:** Enabled

### Virtual Networks and Subnets

#### Virtual Network 1

- **Name:** `my-vnet01`
- **Address Space:** `172.1.0.0/16`
- **Subnet:**
  - **Name:** `my-subnet01`
  - **Address Prefix:** `172.1.0.0/24`

#### Virtual Network 2

- **Name:** `my-vnet02`
- **Address Space:** `10.0.0.0/16`
- **Subnet:**
  - **Name:** `my-subnet02`
  - **Address Prefix:** `10.0.0.0/24`

### Linux Virtual Machine

- **Name:** `myVM1`
- **Location:** `east us`
- **Size:** `Standard_DS1_v2`
- **OS Disk:**
  - **Name:** `myOsDisk`
  - **Caching:** `ReadWrite`
  - **Storage Account Type:** `Premium_LRS`
- **Source Image:** Ubuntu Server 22.04 LTS (Gen2)

## Instructions

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/NashTech-Labs/accessing_aks_securly_with_terraform.git
   cd accessing_aks_securly_with_terraform

