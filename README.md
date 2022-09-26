# Deploy a cloud-native ASP.NET Core microservice with GitHub Actions

Welcome! This is the starter code repository for [this Microsoft Learn Training module](https://docs.microsoft.com/learn/modules/microservices-devops-aspnet-core/). We strongly suggest you follow along with the module for the best results.

# Github Permisions

- ps>`az account show --query 'id' --output tsv`
- ps>`az ad sp create-for-rbac --sdk-auth --name http://eshop-learn-sp.epsilonnet.gr --role Contributor --scopes /subscriptions/de8c9606-2f81-4ce0-9ad8-efd9feb7d97e`
- output
```
{
  "clientId": "5172863c-b903-4e1b-9fb2-8cc4ad915e3d",
  "clientSecret": "e5d5d4c9-d65c-480d-b650-beed454e69c3",
  "subscriptionId": "de8c9606-2f81-4ce0-9ad8-efd9feb7d97e",
  "tenantId": "54a6385f-8ade-4892-a404-d486b55a6746",
  "activeDirectoryEndpointUrl": "https://login.microsoftonline.com",
  "resourceManagerEndpointUrl": "https://management.azure.com/",
  "activeDirectoryGraphResourceId": "https://graph.windows.net/",
  "sqlManagementEndpointUrl": "https://management.core.windows.net:8443/",
  "galleryEndpointUrl": "https://gallery.azure.com/",
  "managementEndpointUrl": "https://management.core.windows.net/"
}
```
- ps>cat ../../config.txt

# Deploy

- ps>`kubectl get pods --selector service=coupon --watch`
- ps>`helm history eshoplearn-coupon`
- ps>`helm rollback eshoplearn-coupon`