
# Deploy ASP.NET application

[![appservice/deploy-aspnet-helloworld/README.md](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/containerapp_aspnet_README_md.yml/badge.svg)](https://github.com/mnriem/csharp-on-azure-examples/actions/workflows/containerapp_aspnet_README_md.yml)

## Prerequisites

This example assumes you have previously completed the following example:

1. [Create an Azure Resource Group](../../group/create/README.md)
1. [Create an Azure Container Apps Environment](../create-environment/)

<!-- workflow.cron(0 11 * * 1) -->
<!-- workflow.include(../create-environment/README.md) -->

## Deploy an ASP.NET application

<!-- workflow.run() 

  cd containerapp/aspnet

 -->

To deploy the ASP.NET container image to Azure Container Apps use the command 
line below.

```shell
  export ACA_ASPNET=aspnet

  az containerapp create \
    --name $ACA_ASPNET \
    --resource-group $RESOURCE_GROUP \
    --environment $ACA_ENVIRONMENT_NAME \
    --image $ACR_NAME.azurecr.io/$ACR_HELLOWORLD_IMAGE \
    --target-port 8080 \
    --ingress 'external' \
    --registry-server $ACR_NAME.azurecr.io \
    --min-replicas 1

  az containerapp show \
    --resource-group $RESOURCE_GROUP \
    --name $ACA_ASPNET \
    --query properties.configuration.ingress.fqdn \
    --output tsv
```

Then open your browser to the URL echoed above and you should see:

```text
Hello World!
```

<!-- workflow.run() 

  cd ../..

 -->

## Cleanup

<!-- workflow.directOnly()

  sleep 120
  export URL=https://$(az containerapp show --resource-group $RESOURCE_GROUP --name $ACA_ASPNET --query properties.configuration.ingress.fqdn --output tsv)
  export RESULT=$(curl $URL)
  az group delete --name $RESOURCE_GROUP --yes || true
  if [[ "$RESULT" != *"custom Glassfish"* ]]; then
    echo "Response did not contain 'custom Glassfish'"
    exit 1
  fi

  -->

Do NOT forget to remove the resources once you are done running the example.

1m
