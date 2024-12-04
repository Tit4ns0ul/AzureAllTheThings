## **Azure Kubernetes Service (AKS) Commands**

Here are some of the most common Azure CLI commands for managing AKS clusters:

## **Creating and Managing AKS Clusters**

- **Creating an AKS Cluster**

```bash
az aks create --name <cluster-name> --resource-group <resource-group-name> --node-count <node-count> --location <location>
```

- **Listing AKS Clusters**

```bash
az aks list
```

- **Showing an AKS Cluster**

```bash
az aks show --name <cluster-name> --resource-group <resource-group-name>
```

- **Deleting an AKS Cluster**

```bash
az aks delete --name <cluster-name> --resource-group <resource-group-name> --yes
```

## **Managing Nodes in AKS Clusters**

- **Scaling a Node Pool**

```bash
az aks scale --name <cluster-name> --resource-group <resource-group-name> --node-pool-name <node-pool-name> --node-count <new-node-count>
```

- **Upgrading a Node Pool**

```bash
az aks upgrade-node-pool --name <cluster-name> --resource-group <resource-group-name> --node-pool-name <node-pool-name>
```

## **Managing Applications in AKS Clusters**

- **Deploying an Application**

```bash
az aks deploy --name <deployment-name> --resource-group <resource-group-name> --namespace <namespace> --file <deployment-file>
```

- **Listing Deployments**

```bash
az aks show deployments --name <cluster-name> --resource-group <resource-group-name> --namespace <namespace>
```

- **Getting Deployment Logs**

```bash
az aks show logs --name <cluster-name> --resource-group <resource-group-name> --namespace <namespace> --pod-name <pod-name> --container-name <container-name>
```

**For a more comprehensive list of Azure AKS commands and detailed usage information, refer to the official Azure CLI documentation:** [https://learn.microsoft.com/en-us/cli/azure/aks](https://www.google.com/url?sa=E&source=gmail&q=https://learn.microsoft.com/en-us/cli/azure/aks)
