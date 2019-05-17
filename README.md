# About

The repository defines the Azure infrastructore required for the deployment of CloudDoor - the Command & Control (CnC)
application for bot management.

# TODO

* Add architectural drawings
* Implement "deploy to azure" button
* Add automatic client version updates
* Make sure that the admin api of the IoT Hub can only be accessed from the cloud. Might need to put it into some vNet or something

# Deploy

## Production environemnt

1. Create a resource group - `az group create --name CloudDoorProdResourceGroup --location northeurope`
2. Deploy the resources - `az group deployment create --resource-group CloudDoorProdResourceGroup --template-file "./azuredeploy.json"`

## Development environment

1. Create a resource group - `az group create --name CloudDoorDevResourceGroup --location northeurope`
2. Deploy the resources - `az group deployment create --resource-group CloudDoorDevResourceGroup --template-file "./azuredeploy.json" --parameters @azuredeploy-devparameters.json`