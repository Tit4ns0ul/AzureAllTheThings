## **Azure Storage Account Commands**

Here are some of the most common Azure CLI commands for managing storage accounts:

- **Creating a Storage Account**

```bash
az storage account create --name <storage-account-name> --resource-group <resource-group-name> --location <location> --sku <sku-name>
```

- **Listing Storage Accounts**

```bash
az storage account list
```

- **Showing a Storage Account**

```bash
az storage account show --name <storage-account-name> --resource-group <resource-group-name>
```

- **Deleting a Storage Account**

```bash
az storage account delete --name <storage-account-name> --resource-group <resource-group-name> --yes
```

## **Managing Storage Account Keys**

```bash
# List keys
az storage account keys list --name <storage-account-name> --resource-group <resource-group-name>

# Regenerate a key
az storage account keys renew --name <storage-account-name> --resource-group <resource-group-name> --key <key-name>
```

## **Managing Storage Account Network Rules**

```bash
# Add a network rule
az storage account network-rule add --name <storage-account-name> --resource-group <resource-group-name> --ip-address <ip-address>

# Remove a network rule
az storage account network-rule remove --name <storage-account-name> --resource-group <resource-group-name> --ip-address <ip-address>
```

## **Managing Storage Account Blob Service**

```bash
# Create a blob container
az storage container create --name <container-name> --account-name <storage-account-name>

# List blobs in a container
az storage blob list --name <container-name> --account-name <storage-account-name>

# Upload a blob
az storage blob upload --file <file-path> --container-name <container-name> --name <blob-name> --account-name <storage-account-name>

# Download a blob
az storage blob download --name <blob-name> --container-name <container-name> --file <file-path> --account-name <storage-account-name>

# Delete a blob
az storage blob delete --name <blob-name> --container-name <container-name> --account-name <storage-account-name>
```

## **Managing Storage Account File Service**

```bash
# Create a file share
az storage share create --name <share-name> --account-name <storage-account-name>

# List files in a share
az storage file list --share-name <share-name> --account-name <storage-account-name>

# Upload a file
az storage file upload --file <file-path> --share-name <share-name> --name <file-name> --account-name <storage-account-name>

# Download a file
az storage file download --name <file-name> --share-name <share-name> --file <file-path> --account-name <storage-account-name>

# Delete a file
az storage file delete --name <file-name> --share-name <share-name> --account-name <storage-account-name>
```

## **Creating and Managing Disk**

- **Creating a Managed Disk**

```bash
az disk create --name <disk-name> --resource-group <resource-group-name> --location <location> --size-gb <size-in-gb> --sku Standard_LRS
```

- **Listing Disks**

```bash
az disk list --resource-group <resource-group-name>
```

- **Showing a Disk**

```bash
az disk show --name <disk-name> --resource-group <resource-group-name>
```

- **Deleting a Disk**

```bash
az disk delete --name <disk-name> --resource-group <resource-group-name> --yes
```

## **Attaching and Detaching Disks to Virtual Machines**

- **Attaching a Disk to a VM**

```bash
az vm disk attach --name <vm-name> --resource-group <resource-group-name> --disk-name <disk-name> --lun <lun-number>
```

- **Detaching a Disk from a VM**

```bash
az vm disk detach --name <vm-name> --resource-group <resource-group-name> --lun <lun-number>
```

**Remember to replace the placeholders like `<storage-account-name>`, `<resource-group-name>`, `<location>`, `<sku-name>`, `<container-name>`, `<blob-name>`, `<file-path>`, and `<file-name>` with your actual values.**

For a more comprehensive list of Azure Storage commands and detailed usage information, refer to the official Azure CLI documentation: [https://learn.microsoft.com/en-us/cli/azure/storage](https://learn.microsoft.com/en-us/cli/azure/storage)
