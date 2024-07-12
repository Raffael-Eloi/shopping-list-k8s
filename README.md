# Shopping List K8S 🚀
This repository contains Terraform code and a configured CI/CD pipeline to deploy infrastructure on Azure for the [Shopping List API](https://github.com/Raffael-Eloi/shopping-list).
The Shopping List API provides a comprehensive solution for managing a shopping list with various features for both customers and store managers. It allows customers to browse products, add items to their cart, and make purchases, while store managers can manage promotions, monitor inventory levels, and receive email notifications.

# Architecture preview 📈
![image](https://github.com/Raffael-Eloi/shopping-list-k8s/assets/51720161/291610a7-ed34-4824-ba87-0f61a0a61245)

# Prerequisites ✅
Ensure you have the following installed before proceeding:
- [Terraform](https://developer.hashicorp.com/terraform/install?product_intent=terraform)
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)
- Access to an Azure account with permissions to create resources

## Running Locally 💻

To deploy the infrastructure locally, follow these steps:

1. **Initialize Terraform:**
   ```sh
   terraform init
   ```
   This command prepares your working directory for other Terraform commands.

2. **Plan the Deployment:**
   ```sh
   terraform plan
   ```
   This command displays the changes required by the current configuration. It provides a preview of what will be added, modified, or deleted in your infrastructure.

3. **Apply the Deployment:**
   ```sh
   terraform apply
   ```
   This command creates or updates the infrastructure. You will need to type `yes` and press enter to confirm the changes.

## Running in the CI/CD Pipeline 🔁

To deploy the infrastructure using the CI/CD pipeline, follow these steps:

1. **Create Azure Credentials:**
   Ensure you have created and configured your Azure credentials. This typically involves creating a service principal and setting the necessary environment variables (`AZURE_CLIENT_ID`, `AZURE_TENANT_ID`, `AZURE_SUBSCRIPTION_ID`).

2. **Modify Configuration:**
   Edit the `resource_group.tf` file to specify the name of your Azure resource group.

3. **Pipeline Execution:**
   The CI/CD pipeline configuration is set up to use these credentials and deploy the infrastructure. Ensure your pipeline is configured to use these environment variables and that it triggers on the necessary events (e.g., push to the main branch).

## License 🌎

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
