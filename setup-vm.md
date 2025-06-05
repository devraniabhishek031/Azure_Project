Create VM using Azure CLI

step1: Start with creating a Resource Group

COMMAND: az group create --name learn-azure-cli --location eastus

Step2:Set the Resource Group as default (Optional)

az config set defaults.group=learn-azure-cli

Step3: Create VM with Vnet

az vm create \
  --resource-group learn-azure-cli \
  --name vmName \ 
  --image Ubuntu2204 \
  --vnet-name default \  
  --subnet default \    
  --generate-ssh-keys \
  --output json \
  --verbose

***Delete the Resource Group to delete all the resources****

az group delete --name learn-azure-cli

