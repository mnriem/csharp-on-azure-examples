
# Create an App Service Plan

## Prerequisites

This example assumes you have previously completed the following example:

1. [Create an Azure Resource Group](../../group/create/README.md)

## Create an App Service Plan

<!-- workflow.cron(0 0 * * 5) -->
<!-- workflow.include(../../group/create/README.md) -->

First, create the environment variable used for our App Service Plan
using the command line below:

<!-- workflow.skip() -->
```shell
  export APPSERVICE_PLAN=csoaz-asp-$RANDOM
```

<!-- workflow.run() 
if [[ -z $APPSERVICE_PLAN ]]; then
  export APPSERVICE_PLAN=csoaz-asp-$RANDOM
  export REGION=westus3
fi
-->

Then, create the App Service Plan using the following command line:

```shell
  az appservice plan create \
    --resource-group $RESOURCE_GROUP \
    --location $REGION \
    --name $APPSERVICE_PLAN \
    --is-linux \
    --sku P1v3
```

<!-- workflow.directOnly() 

  export RESULT=$(az appservice plan show --resource-group $RESOURCE_GROUP --name $APPSERVICE_PLAN --query properties.provisioningState --output tsv)
  az group delete --name $RESOURCE_GROUP --yes || true
  if [[ "$RESULT" != Succeeded ]]; then
    exit 1
  fi
  exit 0

  -->

## Cleanup

Do NOT forget to remove the resources once you are done running the example.

1m
