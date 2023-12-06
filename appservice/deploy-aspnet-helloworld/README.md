
# Deploy ASP.NET Hello World application

## Prerequisites

This example assumes you have previously completed the following example:

1. [Create an Azure Resource Group](../../group/create/README.md)
1. [Create an App Service Plan](../create-plan/)

## Deploy the ASP.NET Hello World application

To create the Hello World application use the following command line:

```shell
  dotnet new web --no-https --exclude-launch-settings
```

Then to validate the application works execute the following command line:

<!-- workflow.skip() -->
```shell
  dotnet run --urls=http://0.0.0.0:8080
```

Now the application is up and running. You can validate it by using your
browser and going to http://localhost:8080/.

The next step is to create the release version of your application. Use the 
command line below to create that version:

```shell
  dotnet publish --runtime linux-x64 --self-contained --configuration Release
```

Next create the zip file that will be used to deploy the application with the
following command lines:

```shell
  cd bin/Release/net8.0/linux-x64/publish
  zip -r deploy.zip *
```

Now you have the `deploy.zip` file necessary for deployment.

The next step is the create the webapp on Azure, execute the following command
lines:

```shell
  export APPSERVICE_HELLOWORLD=csoaz-asp-helloworld-$RANDOM

  az webapp create \
    --resource-group $RESOURCE_GROUP \
    --plan $APPSERVICE_PLAN \
    --name $APPSERVICE_HELLOWORLD \
    --runtime "DOTNETCORE:8.0"
```

Now execute the deploy by using the command line below:

```shell
  az webapp deploy \
    --resource-group $RESOURCE_GROUP \
    --name $APPSERVICE_HELLOWORLD \
    --src-path deploy.zip \
    --type zip
```

## Cleanup

Do NOT forget to remove the resources once you are done running the example.

1m
