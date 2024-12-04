## **Azure Virtual Network (VNet) Commands**

Here are some of the most common Azure CLI commands for managing Azure Virtual Networks:

## **Creating and Managing Virtual Networks**

- **Creating a Virtual Network**

```bash
az network vnet create --name <vnet-name> --resource-group <resource-group-name> --location <location> --address-prefix <address-prefix>
```

- **Listing Virtual Networks**

```bash
az network vnet list --resource-group <resource-group-name>
```

- **Showing a Virtual Network**

```bash
az network vnet show --name <vnet-name> --resource-group <resource-group-name>
```

- **Deleting a Virtual Network**

```bash
az network vnet delete --name <vnet-name> --resource-group <resource-group-name> --yes
```

## **Managing Subnets**

- **Creating a Subnet**

```bash
az network vnet subnet create --name <subnet-name> --vnet-name <vnet-name> --resource-group <resource-group-name> --address-prefix <subnet-address-prefix>
```

- **Listing Subnets**

```bash
az network vnet subnet list --vnet-name <vnet-name> --resource-group <resource-group-name>
```

- **Showing a Subnet**

```bash
az network vnet subnet show --name <subnet-name> --vnet-name <vnet-name> --resource-group <resource-group-name>
```

- **Deleting a Subnet**

```bash
az network vnet subnet delete --name <subnet-name> --vnet-name <vnet-name> --resource-group <resource-group-name> --yes
```

## **Managing Network Security Groups (NSGs)**

- **Creating an NSG**

```bash
az network nsg create --name <nsg-name> --resource-group <resource-group-name> --location <location>
```

- **Listing NSGs**

```bash
az network nsg list --resource-group <resource-group-name>
```

- **Showing an NSG**

```bash
az network nsg show --name <nsg-name> --resource-group <resource-group-name>
```

- **Deleting an NSG**

```bash
az network nsg delete --name <nsg-name> --resource-group <resource-group-name> --yes
```

**For a more comprehensive list of Azure Virtual Network commands and detailed usage information, refer to the official Azure CLI documentation:** [https://learn.microsoft.com/en-us/cli/azure/network](https://www.google.com/url?sa=E&source=gmail&q=https://learn.microsoft.com/en-us/cli/azure/network)
