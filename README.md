# Azure Private Link DNS Forwarders

This solution will deploy two Windows DNS servers in an Availability Set, configure a DNS Conditional Forwarder for Azure Storage, and configure a DNS Forwarder to your on premise DNS servers.

## Assumptions

Your DNS servers are on premise and you need DNS servers in Azure to support Private Link.

## Deployment Options

### Try with Azure Portal

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjamasten%2FAzurePrivateLinkDnsForwarders%2Fmain%2Fsolution.json)
[![Deploy to Azure Gov](https://aka.ms/deploytoazuregovbutton)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fjamasten%2FAzurePrivateLinkDnsForwarders%2Fmain%2Fsolution.json)

### Try with PowerShell

````powershell
New-AzResourceGroupDeployment `
    -ResourceGroupName '<Resource Group Name>' `
    -TemplateUri 'https://raw.githubusercontent.com/jamasten/AzurePrivateLinkDnsForwarders/main/solution.json'
````

### Try with CLI

````cli
az deployment group create \
    --resource-group '<Resource Group Name>' \
    --template-uri 'https://raw.githubusercontent.com/jamasten/AzurePrivateLinkDnsForwarders/main/solution.json' \
    --parameters \
        AvSetName '<Availability Set Name>'
````
