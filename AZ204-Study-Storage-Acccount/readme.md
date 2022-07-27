# Manual Deployment
```az login```

```az account list --all --output table```

```az account set --subscription "---your subscription id between quotes here---"```

```az group create --name az204-arm-rg --location westus```

```az  deployment group create --resource-group az204-arm-rg --template-file azuredeploy.json --parameters azuredeploy.parameters.json```

## Commands to verify 
```az storage account show --resource-group az204-arm-rg --name yatesaz204storageacctarm```

Notes
-	The subscription id should change based on what you see when the account list is printed out.


# Deploy with button
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmadcodemonkey%2FAzure-ARM-Templates%2Fmain%2FAZ204-Study-Storage-Acccount%2Fazuredeploy.json)

The URL to the ARM json file (raw view) is URL-encoded so that it using this PowerShell command
```
$url = "https://raw.githubusercontent.com/madcodemonkey/Azure-ARM-Templates/main/AZ204-Study-Storage-Acccount/azuredeploy.json"
[uri]::EscapeDataString($url)
```
which outputs
```
https%3A%2F%2Fraw.githubusercontent.com%2Fmadcodemonkey%2FAzure-ARM-Templates%2Fmain%2FAZ204-Study-Storage-Acccount%2Fazuredeploy.json
```

Read more [here](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-to-azure-button)
