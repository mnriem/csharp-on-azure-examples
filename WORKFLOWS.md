# Workflows

<!-- 

  Creating / updating the service principal for GitHub Actions:

  az ad sp create-for-rbac --name csoaz-github-actions --role Owner --scopes /subscriptions/<subscription-id> --sdk-auth

 -->

# Workflows

| Category | Example     | Workflow Status | Schedule |
| -------- | ----------- | --------------- | -------- |
| Azure Resource Group examples | Create an Azure Resource Group | [![group/create/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/group_create_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/group_create_README_md.yml) | 0 1 * * 1 |
| Azure App Service examples | Create an App Service Plan |[ ![appservice/create-plan/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/appservice_create-plan_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/appservice_create-plan_README_md.yml) | 0 2 * * 1 |
| | Delete an App Service plan | [![appservice/delete-plan/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/appservice_delete-plan_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/appservice_delete-plan_README_md.yml) | 0 3 * * 1 |
| | Deploy an ASP.NET Hello World application | [![appservice/deploy-aspnet-helloworld/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/appservice_deploy-aspnet-helloworld_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/appservice_deploy-aspnet-helloworld_README_md.yml) | 0 4 * * 1 |
| Azure Container Registry examples | Create an Azure Container Registry | [![acr/create/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_create_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_create_README_md.yml) | 0 5 * * 1 |
| Azure Key Vault examples | Create an Azure Key Vault | [![keyvault/create/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/keyvault_create_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/keyvault_create_README_md.yml) | 0 6 * * 1 |
| | Adding a Secret to Azure Key Vault | [![keyvault/add-secret/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/keyvault_add-secret_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/keyvault_add-secret_README_md.yml) | 0 7 * * 1 |
| Azure Container Registry examples | Build and push ASP.NET Hello World application | [![acr/create/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_aspnet-helloworld_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_aspnet-helloworld_README_md.yml) | 0 8 * * 1 |
| Azure Key Vault examples | Create a self-signed certificate | [![keyvault/create-self-signed-certificate/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/keyvault_create-self-signed-certificate_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/keyvault_create-self-signed-certificate_README_md.yml) | 0 9 * * 1 |
| Azure Container App examples | Create an environment | [![containerapp/create-environment/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/containerapp_create-environment_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/containerapp_create-environment_README_md.yml) | 0 10 * * 1 |
| Azure Container App examples | Deploy an ASP.NET application | [![containerapp/create-environment/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/containerapp_aspnet_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/containerapp_aspnet_README_md.yml) | 0 11 * * 1 |
