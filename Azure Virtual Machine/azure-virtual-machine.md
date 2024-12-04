## **Azure Virtual Machine Commands: A Comprehensive Overview**

Azure offers a robust set of commands to manage virtual machines (VMs) via the Azure CLI and PowerShell. Here's a breakdown of the most common commands and their functions:

## **Managing VM State:**

- **Start a VM:**
  ```bash
  az vm start --resource-group myResourceGroup --name myVM
  ```
- **Stop a VM:**
  ```bash
  az vm stop --resource-group myResourceGroup --name myVM
  ```
- **Deallocate a VM:**
  ```bash
  az vm deallocate --resource-group myResourceGroup --name myVM
  ```
- **Restart a VM:**
  ```bash
  az vm restart --resource-group myResourceGroup --name myVM
  ```
- **Redeploy a VM:**
  ```bash
  az vm redeploy --resource-group myResourceGroup --name myVM
  ```
- **Delete a VM:**
  ```bash
  az vm delete --resource-group myResourceGroup --name myVM
  ```

## **Disk and Image Management:**

- **Add a data disk to a VM:**
  ```bash
  az vm disk attach --resource-group myResourceGroup --vm-name myVM --disk myDataDisk --size-gb 128 --new
  ```
- **List attached disks to a VM:**
  ```bash
  az vm show --resource-group groupName --name vmName --query "storageProfile"
  ```
- **Remove a data disk from a VM:**
  ```bash
  az vm disk detach --resource-group myResourceGroup --vm-name myVM --disk myDataDisk
  ```
- **Resize a disk:**
  ```bash
  az disk update --resource-group myResourceGroup --name myDataDisk --size-gb 256
  ```
- **Snapshot a disk:**
  ```bash
  az snapshot create --resource-group myResourceGroup --name mySnapshot --source myDataDisk
  ```
- **Create image of a VM:**
  ```bash
  az image create --resource-group myResourceGroup --source myVM --name myImage
  ```
- **Create VM from image:**
  ```bash
  az vm create --resource-group myResourceGroup --name myNewVM --image myImage
  ```

## **Azure PowerShell Commands:**

**Getting Information:**

- **List VMs in a subscription:**
  ```powershell
  Get-AzVM
  ```
- **List VMs in a resource group:**
  ```powershell
  Get-AzVM -ResourceGroupName $myResourceGroup
  ```
- **Get information about a VM:**
  ```powershell
  Get-AzVM -ResourceGroupName $myResourceGroup -Name $myVM
  ```

## **Managing VMs:**

- **Start a VM:**
  ```powershell
  Start-AzVM -ResourceGroupName $myResourceGroup -Name $myVM
  ```
- **Stop a VM:**
  ```powershell
  Stop-AzVM -ResourceGroupName $myResourceGroup -Name $myVM
  ```
- **Restart a running VM:**
  ```powershell
  Restart-AzVM -ResourceGroupName $myResourceGroup -Name $myVM
  ```
- **Delete a VM:**
  ```powershell
  Remove-AzVM -ResourceGroupName $myResourceGroup -Name $myVM
  ```

## **Additional Considerations:**

- **Azure Portal:** A user-friendly interface to manage VMs without command-line tools.
- **Azure Resource Manager:** The underlying framework for managing Azure resources, including VMs.
- **Azure Automation:** For automating VM management tasks using scripts and workflows.
- **Azure Policy:** For enforcing compliance and security policies on VMs.

Remember to consult the official Azure documentation for the most up-to-date information and detailed command usage.
