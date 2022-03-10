
# Install Az PowerShell module

## Prerequisites

This example assume you are logged into Azure using PowerShell and have set your
default subscription, if you have NOT done so please go to our top-level
[README](../../)

<!-- workflow.cron(0 1 * * 0) -->

## Install Az PowerShell module

To install the Az Powershell module use the command line below:

```shell
  Install-Module -Name Az -Scope CurrentUser -Repository PSGallery -Force
```

## Cleanup

Do NOT forget to remove the resources once you are done running the example.
