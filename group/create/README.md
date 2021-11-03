
# Create an Azure Resource Group

## Prerequisites

This example assume you are logged into Azure using PowerShell and have set your
default subscription, if you have NOT done so please go to our top-level
[README](../../)

## Create the Resource Group

To setup the environment variables needed to create the Resource Group execute
the command lines below:

```shell
  $env:RESOURCE_GROUP='csharp-on-azure'
  $env:REGION='westus2'
```

To create the Resource Group use the following command line:

```shell
  New-AzResourceGroup -Name $env:RESOURCE_GROUP -Location $env:REGION
```

## Cleanup

Do NOT forget to remove the resources once you are done running the example.

1m
