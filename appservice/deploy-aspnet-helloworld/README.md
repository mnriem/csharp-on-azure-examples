
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
  dotnet run --urls=http://0.0.0.0:5000 
```

Now the application is up and running. You can validate it by using your
browser and going to http://localhost:5000/.

The next step is to create the release version of your application. Use the 
command line below to create that version:

```shell
  dotnet publish --configuration Release
```

Next create the zip file that will be used to deploy the application with the
following command lines:

```shell
  cd bin\Release\net6.0\publish
  Compress-Archive -Path * -DestinationPath deploy.zip
```

Now you have the `deploy.zip` file necessary for deployment.

The next step is the create the webapp on Azure, execute the following command
lines:

```shell
  $env:APPSERVICE_ASPNET_HELLOWORLD='appservice-aspnet-helloworld-' + (Get-Random -Maximum 1000)
  New-AzWebApp `
    -ResourceGroupName $env:RESOURCE_GROUP `
    -AppServicePlan $env:APPSERVICE_PLAN `
    -Name $env:APPSERVICE_ASPNET_HELLOWORLD
```

Now execute the deploy by using the command line below:

```shell
  Publish-AzWebApp `
    -ResourceGroupName $env:RESOURCE_GROUP `
    -Name $env:APPSERVICE_ASPNET_HELLOWORLD `
    -ArchivePath (Get-Item .\deploy.zip).FullName `
    -Force
```

## Cleanup

Do NOT forget to remove the resources once you are done running the example.

1m
