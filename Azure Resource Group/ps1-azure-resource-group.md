## **Azure Group Commands**

Azure Resource Groups are containers that hold related Azure resources. Here are the primary PowerShell commands for managing resource groups:

- **Creating a Resource Group**

```Bash
az group create --name MyResourceGroup --location EastUS
```

- **Deleting a Resource Group**

```Bash
az group delete --name MyResourceGroup
```

- **Listing Resource Groups**

```Bash
az group list
```

- **Showing a Resource Group**

```Bash
az group show --name MyResourceGroup
```

- **Updating a Resource Group**

```Bash
az group update --name MyResourceGroup --tags Department=IT,Environment=Prod
```

- **Checking Resource Group Existence**

```Bash
az group exists --name MyResourceGroup
```

## **Additional Commands**

- **Exporting a Resource Group Template**

```Bash
az group export --name MyResourceGroup --output file.json
```

- **Locking a Resource Group**

```Bash
az group lock create --name MyResourceGroup --lock-type CanNotDelete
```

- **Unlocking a Resource Group**

```Bash
az group lock delete --name MyResourceGroup --lock-name MyLockName
```

## **Working with Deployments**

Azure CLI also provides commands to manage deployments within a resource group:

- **Creating a Deployment**

```Bash
az group deployment create --name MyDeployment --resource-group MyResourceGroup --template-file template.json --parameters parameters.json
```

- **Listing Deployments**

```Bash
az group deployment list --resource-group MyResourceGroup
```

- **Showing a Deployment**

```Bash
az group deployment show --name MyDeployment --resource-group MyResourceGroup
```

- **Deleting a Deployment**

```Bash
az group deployment delete --name MyDeployment --resource-group MyResourceGroup
```

## **Remember**

- Always replace MyResourceGroup with the actual name of your resource group.
- Use the --help flag with any command to get detailed usage information.
- For more advanced scenarios, consider using Azure PowerShell or Azure Resource Manager templates.

By effectively using these commands, you can efficiently manage your Azure resources within resource groups.
