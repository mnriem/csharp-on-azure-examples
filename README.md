# C# on Azure Examples

This GitHub repository contains a set of Azure examples specifically for C# 
developers on macOS / Linux to quickly get started with Azure. Please use the issue tracker to
leave feedback, file issues or to propose other examples.

## Getting started

To work with these examples it is assumed you have the Azure CLI installed, and
you have logged in and set your default subscription. If you haven't done so
follow the steps below.

_Note: Logging in and setting your default subscription needs to be done once 
 per terminal session._

### Install Azure CLI

To setup the Azure CLI, please visit 
[Install the Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli).
And once you are done come back to this README.

### Login into Azure

<!-- workflow.skip() -->
````shell
  az login
````

### Set your default subscription

Get a list of your subscriptions (notice the `refresh` parameter that retrieves up-to-date subscriptions from the server) :

<!-- workflow.skip() -->
````shell
  az account list --output table --refresh
````

Set your default subscription for this session using the subscription id from the previous output:

<!-- workflow.skip() -->
````shell
  az account set --subscription "subscription-id"
````

<!-- workflow.run() 

  exit 0

  -->

## Examples

1. [Azure App Service examples](appservice/README.md)
1. [Azure Container Apps examples](containerapp/README.md)
1. [Azure Container Registry examples](acr/README.md)
1. [Azure Key Vault examples](keyvault/README.md)
1. [Azure Resource Group examples](group/README.md)
