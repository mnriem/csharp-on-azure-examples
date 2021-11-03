# C# on Azure Examples

This GitHub repository contains a set of Azure examples specifically for C# 
developers to quickly get started with Azure. Please use the issue tracker to
leave feedback, file issues or to propose other examples.

## Getting started

To work with these examples it is assumed you have the Azure Az PowerShell 
module installed, and you have logged in and set your default subscription. 
If you haven't done so follow the steps below.

_Note logging in and setting your default subscription needs to be done once per
 terminal session._

### Install PowerShell

If you need to install PowerShell, please visit [Install PowerShell on Windows, Linux and macOS](https://docs.microsoft.com/powershell/scripting/install/installing-powershell).
And once you are done come back to this README.

### Install Azure Az PowerShell module

To setup the Azure Az PowerShell module, please visit [Install the Azure Az PowerShell module](https://docs.microsoft.com//powershell/azure/install-az-ps).
And once you are done come back to this README.

### Login into Azure

<!-- workflow.skip() -->
```shell
  Connect-AzAccount
```

### Set your default subscription

Get a list of your subscriptions

<!-- workflow.skip() -->
```shell
  Get-AzSubscription
```

Set your default subscription for this session using the subscription id from 
the previous output

<!-- workflow.skip() -->
```shell
  $context = Get-AzSubscription -SubscriptionId <subscription id>
  Set-AzContext $context
```

<!-- workflow.run() 
exit 0
  -->

## Azure Resource Group examples

| Name | Link | Status
| ---- | ---- | ------ 
| 1. [Create a Resource Group](group/create/README.md) | | 
