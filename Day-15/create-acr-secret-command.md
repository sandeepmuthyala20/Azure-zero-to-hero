# Command to login to the AKS Cluster

az aks get-credentials --name azuredevops --overwrite-existing --resource-group azurecicd

# Command to get secrets for argocd

kubectl get secrets -n argocd
kubectl edit secret argocd-initial-admin-secret -n argocd
muthyalasandeep@Sandeeps-MacBook-Air Downloads % echo My02amE3alM3dkRCNlBRcg== | base64 --decode
3-6ja7jS7vDB6PQr%                                                                                                                                muthyalasandeep@Sandeeps-MacBook-Air Downloads % 

argocd credentials
username - admin
password - 3-6ja7jS7vDB6PQr

# chane argocd-seerver to NodePort
kubectl edit svc argocd-server -n argocd


# Connect to argocd using browser

Argocd node external IP:port
https://4.154.179.64:31344/

open 31344 port in vmss instances to use the argocd


# Command to create ACR ImagePullSecret

```
kubectl create secret docker-registry <secret-name> \
    --namespace <namespace> \
    --docker-server=<container-registry-name>.azurecr.io \
    --docker-username=<service-principal-ID> \
    --docker-password=<service-principal-password>
```
