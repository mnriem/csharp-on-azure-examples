
# Delete an App Service Plan

## Prerequisites

This example assumes you have previously completed the following example:

1. [Create an Azure Resource Group](../group/create/)
1. [Create an Azure App Service Plan](../create-plan/)

## Delete an App Service Plan

<!-- workflow.include(../create-plan/README.md) -->

To delete the Azure App Service Plan use the following command line:

```shell
  Remove-AzAppServicePlan `
    -Name $env:APPSERVICE_PLAN `
```

## Cleanup

Do NOT forget to remove the resources once you are done running the example.
