```
$ az aks nodepool add `
     --resource-group aks-cluster `
     --cluster-name aks-cluster `
     --name appsnodepool `
     --node-count 5 `
     --node-vm-size Standard_B2ms `
     --kubernetes-version 1.20.7 `
     --max-pods 30 `
     --priority Regular `
     --zones 3 `
     --mode User


az aks nodepool list --resource-group rg-private-aks --cluster-name private-aks


az aks nodepool list --resource-group rg-private-aks --cluster-name private-aks -o table

kubectl get node/aks-appsnodepool-93043827-vmss000000 -o json | jq '.metadata.labels'
```

#### https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/kubernetes-nodepools-explained/ba-p/2531581
