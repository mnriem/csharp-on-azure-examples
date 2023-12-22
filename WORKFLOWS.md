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
| Azure Container Registry | Create an Azure Container Registry | [![acr/create/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_create_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_create_README_md.yml) | 0 5 * * 1 |
