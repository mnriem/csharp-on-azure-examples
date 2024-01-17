
# Build and push ASP.NET Hello World application

[![appservice/deploy-aspnet-helloworld/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_aspnet-helloworld_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/acr_aspnet-helloworld_README_md.yml)

## Prerequisites

This example assumes you have previously completed the following example:

1. [Create an Azure Resource Group](../../group/create/README.md)
1. [Create an Azure Container Registry](../create/README.md)

<!-- workflow.cron(0 4 * * 1) -->
<!-- workflow.include(../create/README.md) -->

## Build and push the ASP.NET Hello World application

<!-- workflow.run() 

  cd acr/aspnet-helloworld

 -->

To test out the Hello World use the command-line below:

<!-- workflow.skip() -->
```shell
  dotnet run --urls=http://0.0.0.0:8080
```

Now the application is up and running. You can validate it by using your
browser and going to http://localhost:8080/.

To create a release version of the application use the following
command-line:

```shell
  dotnet publish --runtime linux-x64 -p:PublishSingleFile=true --self-contained --configuration Release
```

## Build and push the Docker image to your Azure Container Registry

To build and push the Docker image to your ACR use the command line below:

```shell
  export ACR_HELLOWORLD_IMAGE=helloworld:latest

  az acr build --resource-group $RESOURCE_GROUP --registry $ACR_NAME --image $ACR_HELLOWORLD_IMAGE .
```

<!-- workflow.run() 

  cd ../..

 -->

## Cleanup

<!-- workflow.directOnly() 

  az group delete --name $RESOURCE_GROUP --yes || true

  -->

Do NOT forget to remove the resources once you are done running the example.

1m
