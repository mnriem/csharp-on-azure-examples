
# Create an App Service Plan

## Prerequisites

This example assumes you have previously completed the following example:

1. [Create an Azure Resource Group](../../group/create/)

## Create an App Service Plan

First, create the environment variable used for our App Service Plan
using the command line below:

```shell
  $env:APPSERVICE_PLAN='appservice-plan'
```

Then, create the App Service Plan using the following command line:

```shell
  New-AzAppServicePlan `
    -Name $env:APPSERVICE_PLAN `
    -ResourceGroupName $env:RESOURCE_GROUP `
    -Location $env:REGION `
    -Linux `
    -Tier "PremiumV3"
```

## Cleanup

Do NOT forget to remove the resources once you are done running the example.

1m
