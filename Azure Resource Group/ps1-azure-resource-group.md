## **Azure Group Commands**

Azure Resource Groups are containers that hold related Azure resources. Here are the primary PowerShell commands for managing resource groups:

- **Creating a Resource Group**

```powershell
New-AzResourceGroup -Name MyResourceGroup -Location "Central India"
```

- **Deleting a Resource Group**

```powershell
Remove-AzResourceGroup -Name MyResourceGroupName -Force
```

- **Listing Resource Groups**

```powershell
Get-AzResourceGroup
```

- **Showing a Resource Group**

```powershell
Get-AzResourceGroup -Name MyResourceGroupName
```

- **Updating a Resource Group**

```powershell
Set-AzResourceGroup -Name MyResourceGroup -Tag @{ Environment = "Production"; Owner = "Admin" }
```

- **Checking Resource Group Existence**

```powershell
try {
    Get-AzResourceGroup -Name MyResourceGroup
    Write-Output "Resource group 'MyResourceGroup' exists."
} catch {
    Write-Output "Resource group 'MyResourceGroup' does not exist."
}
```

## **Additional Commands**

- **Exporting a Resource Group Template**

```powershell
Export-AzResourceGroup -ResourceGroupName MyResourceGroup -Path C:\Templates\file.json
```

- **Locking a Resource Group**
- 
```powershell
New-AzResourceGroupLock -ResourceGroupName MyResourceGroup -LockLevel CanNotDelete -Notes "Locking to prevent accidental deletion"

New-AzResourceGroupLock -ResourceGroupName MyResourceGroup -LockLevel ReadOnly -Notes "Locking for auditing"
```

- **Unlocking a Resource Group**

```powershell
az group lock delete --name MyResourceGroup --lock-name MyLockName
```

## **Working with Deployments**

Azure CLI also provides commands to manage deployments within a resource group:

- **Creating a Deployment**

```powershell
az group deployment create --name MyDeployment --resource-group MyResourceGroup --template-file template.json --parameters parameters.json
```

- **Listing Deployments**

```powershell
az group deployment list --resource-group MyResourceGroup
```

- **Showing a Deployment**

```powershell
az group deployment show --name MyDeployment --resource-group MyResourceGroup
```

- **Deleting a Deployment**

```powershell
az group deployment delete --name MyDeployment --resource-group MyResourceGroup
```

## **Remember**

- Always replace MyResourceGroup with the actual name of your resource group.
- Use the --help flag with any command to get detailed usage information.
- For more advanced scenarios, consider using Azure PowerShell or Azure Resource Manager templates.

By effectively using these commands, you can efficiently manage your Azure resources within resource groups.
