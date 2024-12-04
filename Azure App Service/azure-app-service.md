## **Azure App Service Commands**

Here are some of the most common Azure CLI commands for managing App Service:

## **Creating and Managing App Service Plans**

- **Creating an App Service Plan**

```bash
az appservice plan create --name <plan-name> --resource-group <resource-group-name> --location <location> --sku <sku-name>
```

- **Listing App Service Plans**

```bash
az appservice plan list
```

- **Showing an App Service Plan**

```bash
az appservice plan show --name <plan-name> --resource-group <resource-group-name>
```

- **Deleting an App Service Plan**

```bash
az appservice plan delete --name <plan-name> --resource-group <resource-group-name> --yes
```

## **Creating and Managing Web Apps**

- **Creating a Web App**

```bash
az webapp create --name <app-name> --resource-group <resource-group-name> --plan <plan-name>
```

- **Listing Web Apps**

```bash
az webapp list
```

- **Showing a Web App**

```bash
az webapp show --name <app-name> --resource-group <resource-group-name>
```

- **Starting a Web App**

```bash
az webapp start --name <app-name> --resource-group <resource-group-name>
```

- **Stopping a Web App**

```bash
az webapp stop --name <app-name> --resource-group <resource-group-name>
```

- **Restarting a Web App**

```bash
az webapp restart --name <app-name> --resource-group <resource-group-name>
```

- **Deploying to a Web App**

```bash
az webapp deploy --name <app-name> --resource-group <resource-group-name> --package <path-to-package>
```

## **Configuring Web Apps**

- **Setting Application Settings**

```bash
az webapp config appsettings set --name <app-name> --resource-group <resource-group-name> --settings <key1=value1;key2=value2>
```

- **Setting Connection Strings**

```bash
az webapp config connection-string set --name <app-name> --resource-group <resource-group-name> --connection-string <key1=value1;key2=value2>
```

- **Adding a Custom Domain**

```bash
az webapp config hostname add --name <app-name> --resource-group <resource-group-name> --hostname <domain-name>
```

## **Managing Deployment Slots**

- **Creating a Deployment Slot**

```bash
az webapp slot create --name <app-name> --resource-group <resource-group-name> --slot-name <slot-name>
```

- **Swapping Deployment Slots**

```bash
az webapp slot swap --name <app-name> --resource-group <resource-group-name> --slot-name <slot-name>
```

- **Deleting a Deployment Slot**

```bash
az webapp slot delete --name <app-name> --resource-group <resource-group-name> --slot-name <slot-name>
```

**Remember to replace the placeholders like `<app-name>`, `<plan-name>`, `<resource-group-name>`, `<location>`, `<sku-name>`, `<domain-name>`, `<slot-name>`, and `<path-to-package>` with your actual values.**

For a more comprehensive list of Azure App Service commands and detailed usage information, refer to the official Azure CLI documentation: [https://learn.microsoft.com/en-us/azure/app-service/overview-hosting-plans](https://learn.microsoft.com/en-us/azure/app-service/overview-hosting-plans)
