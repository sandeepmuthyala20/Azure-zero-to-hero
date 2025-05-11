# Command to login to the AKS Cluster

az aks get-credentials --name azuredevops --overwrite-existing --resource-group azurecicd

# Command to create ACR ImagePullSecret

```
kubectl create secret docker-registry <secret-name> \
    --namespace <namespace> \
    --docker-server=<container-registry-name>.azurecr.io \
    --docker-username=<service-principal-ID> \
    --docker-password=<service-principal-password>
```
