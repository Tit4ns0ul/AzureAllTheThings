# **Get-AzureRM vs Get-Az**

Azure PowerShell cmdlets are used to manage resources in Microsoft Azure. There are two main modules for working with Azure resources in PowerShell: **AzureRM** and **Az**. While **AzureRM** was used in the past, **Az** is the new, cross-platform module that replaces it.

## **1. `Get-AzureRM`**

`Get-AzureRM` cmdlets are part of the older **AzureRM** module, which was used for managing Azure resources before the introduction of the **Az** module.

### Key Points:
- **AzureRM** is being deprecated, and support for it is limited.
- The module was used for managing resources before the move to the **Az** module.
- Only available for Windows.

### Example Command:
```powershell
Get-AzureRMResourceGroup
```

# **Get-Az**
Get-Az cmdlets are part of the newer Az module, which is the recommended module for managing Azure resources. It is fully cross-platform and works on Windows, macOS, and Linux.

Key Points:
Az is the successor of AzureRM and is the actively maintained module.
Fully supports cross-platform environments (Windows, Linux, macOS).
Better performance and includes enhanced cmdlets for newer Azure services.
Example Command:

```powershell
Get-AzResourceGroup
```
This cmdlet retrieves all resource groups in your Azure subscription using the Az module.



# **When to Use Get-Az vs Get-AzureRM**
- **Use Get-Az for new projects or when setting up new environments as it supports cross-platform use and all modern Azure services.**
- **Use Get-AzureRM if you are working with older scripts or need backward compatibility, though it is advisable to migrate to Az as AzureRM is deprecated.**


## **Conclusion**
-The Az module is the future of Azure PowerShell. It is recommended to migrate your scripts and processes from AzureRM to Az to ensure ongoing support and better compatibility with newer Azure features.
