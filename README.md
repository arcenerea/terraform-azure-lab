# ☁️ Terraform Azure Lab

Infrastructure as Code on Microsoft Azure using Terraform. Deploys a complete environment including resource groups, virtual networks, subnets, network security groups and a virtual machine.

Built and documented by [Nerea Arce](https://www.linkedin.com/in/nerea-arce/) · SysAdmin & DevOps Engineer

---

## What this lab deploys

| Resource | Description |
|----------|-------------|
| Resource Group | Logical container for all resources |
| Virtual Network | Isolated network with custom address space |
| Subnet | Segmented network within the VNet |
| Network Security Group | Firewall rules for inbound/outbound traffic |
| Public IP | Static public IP address |
| Network Interface | Connects the VM to the network |
| Linux Virtual Machine | Ubuntu 20.04 LTS with SSH access |
| Storage Account | Blob storage for diagnostics and backups |

---

## Repository structure

    terraform-azure-lab/
    ├── main.tf           # Main infrastructure definition
    ├── variables.tf      # Input variables
    ├── outputs.tf        # Output values
    ├── providers.tf      # Azure provider configuration
    └── README.md

---

## Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/install) >= 1.0
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)
- An active Azure subscription

---

## Usage

Authenticate with Azure:

    az login

Initialise Terraform:

    terraform init

Preview the changes:

    terraform plan

Deploy the infrastructure:

    terraform apply

Destroy the infrastructure when done:

    terraform destroy

---

## Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `location` | Azure region | `swedencentral` |
| `resource_group_name` | Name of the resource group | `rg-terraform-lab` |
| `vm_size` | Size of the virtual machine | `Standard_B1s` |
| `admin_username` | VM admin username | `azureuser` |

---

## Outputs

| Output | Description |
|--------|-------------|
| `public_ip` | Public IP address of the virtual machine |
| `resource_group_name` | Name of the deployed resource group |
| `vm_name` | Name of the virtual machine |

---

## Tech stack

![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

## Author

**Nerea Arce** — SysAdmin · DevOps · Cloud Infrastructure

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nerea-arce/)
[![GitHub](https://img.shields.io/badge/GitHub-arcenerea-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/arcenerea)
