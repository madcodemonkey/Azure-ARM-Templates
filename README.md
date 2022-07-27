# Azure-ARM-Templates

## Commands used to deploy 
```az login```

```az account list --all --output table```

```az account set --subscription "---your subscription id between quotes here---"```

```az group create --name az204-arm-rg --location westus```

```az  deployment group create --resource-group az204-arm-rg --template-file azuredeploy.json --parameters azuredeploy.parameters.json```

## Commands to verify 
```az storage account show --resource-group az204-arm-rg --name yatesaz204storageacctarm```

Notes
-	The subscription id should change based on what you see when the account list is printed out.


## References
- [How to create a deploy button for ARM templates](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-to-azure-button)
