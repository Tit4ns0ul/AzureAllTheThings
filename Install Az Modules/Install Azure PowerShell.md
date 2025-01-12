## **Install Azure PowerShell Modules Commands**

To install ## **Azure PowerShell** you can follow these steps. Azure PowerShell is a set of cmdlets for managing Azure resources directly from the command line:

- **Step 1: Open PowerShell as Administrator**

- Make sure to run PowerShell with elevated (administrator) privileges to avoid permission issues during installation.

- **Step 2: Install the Az Module**

- To install the `Az` module, use the following command:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

- **Step 3: Verify the Installation**

```powershell
Get-InstalledModule -Name Az
```

- **Step 4: Import the Az Module (If Needed)**

```powershell
Import-Module Az
```

- **Step 5: Log in to Azure**

```powershell
Connect-AzAccount
```
- **Step 6: Update Azure PowerShell (Optional)**

```powershell
Update-Module -Name Az
```


## **Remember**

- **Use the --help flag with any command to get detailed usage information. For example:**

```powershell
Get-Help Install-Module --full
```
- **Always run PowerShell as Administrator to avoid permission issues when installing or updating modules.**
- Use -Scope CurrentUser if you don't want to install the module system-wide (useful in cases where you don't have admin rights):
  
```powershell
Install-Module -Name Az -AllowClobber -Force -Scope CurrentUser
```

- **Check for updates regularly to keep your Azure PowerShell up-to-date:**
```powershell
Update-Module -Name Az
```

- **Use Get-InstalledModule to check the version of installed modules and ensure that the correct version is being used.**
- If you face issues during installation, ensure that your PowerShell version is updated. You can check the version with:
  
```powershell
$PSVersionTable.PSVersion
```
- Be aware of cross-platform support: The Az module works on Windows, Linux, and macOS, while older modules like AzureRM were limited to Windows only.


- **Consider using Set-ExecutionPolicy if you encounter issues related to running scripts:**
```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
- Avoid using AzureRM: The AzureRM module is deprecated, and it is strongly recommended to transition to Az for compatibility and performance improvements.


- **Use Get-Help <Cmdlet> for any command to access its documentation:**
```powershell
Get-Help Connect-AzAccount
```

- By following these best practices, you will ensure that your Azure PowerShell environment is stable, secure, and up to date.

