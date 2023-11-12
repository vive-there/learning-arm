# Learning ARM

## Deploy ARM to create storage account
az deployment group create \
--resource-group learn-arm \
--template-file ./c1/azdeploy-sa.json \
--name DeployStorageAccount \
--parameters './c1/params-sa.json' storageAccountName=vivethere$RANDOM

## Deploy
keyVaultName=VivethereKV$RANDOM
az deployment group create \
--name KeyVaultDeployment$RANDOM \
--resource-group learn-arm \
--template-file './c1/azdeploy-kv-and-secret.json' \
--parameters keyVaultName=$keyVaultName secretName=AwesomeApiKey secretValue=blablabla$RANDOM



## Reference
https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/deploy-cli
