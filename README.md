# Learning ARM

## Deploy ARM to create storage account
az deployment group create \
--resource-group learn-arm \
--template-file ./c1/azdeploy-sa.json \
--name DeployStorageAccount \
--parameters './c1/params-sa.json' storageAccountName=vivethere$RANDOM

## Reference
https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-cli
