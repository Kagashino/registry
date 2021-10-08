---
title: Azure Classic
meta_desc: Learn how to use Pulumi's Azure Classic Provider to reduce the complexity of managing and provisioning Azure resources with Azure Resource Manager (ARM) APIs.
layout: overview
---

{{% notes %}}
We recommend using the [Azure Native provider]({{< relref "/registry/packages/azure-native" >}}) to provision Azure infrastructure. Azure Native provides complete coverage of Azure resources and same-day access to new resources and resource updates because it’s built and automatically from the Azure Resource Manager API.

Azure Classic is based on the Terraform AzureRM provider. It has fewer resources and resource options and receives new Azure features more slowly than Azure Native. However, Azure Classic remains fully supported for existing usage.
{{% /notes %}}

The Azure Classic provider for Pulumi can be used to provision many of the cloud resources available in [Azure](https://azure.microsoft.com/en-us/). It manages and provisions resources using the [Azure Resource Manager (ARM) APIs](https://docs.microsoft.com/en-us/rest/api/resources/).

Azure Classic must be configured with credentials to deploy and update resources in Azure; see the [Installation & Configuration page]({{<relref "./installation-configuration">}}) for instructions.

## Example

```javascript
const azure = require("@pulumi/azure")

const resourceGroupName = new azure.core.ResourceGroup("my-group", {
    location: "westus2",
});
```

Visit the [How-to Guides page]({{<relref "./how-to-guides">}}) to find step-by-step guides for specific scenarios like running an app in Azure App Service or setting up a serverless Azure Function.

## SDK packages

The Azure Classic provider is available as a package in all Pulumi languages:

* JavaScript/TypeScript: [`@pulumi/azure`](https://www.npmjs.com/package/@pulumi/azure)
* Python: [`pulumi-azure`](https://pypi.org/project/pulumi-azure/)
* Go: [`github.com/pulumi/pulumi-azure/sdk/v4/go/azure`](https://github.com/pulumi/pulumi-azure)
* .NET: [`Pulumi.Azure`](https://www.nuget.org/packages/Pulumi.Azure)