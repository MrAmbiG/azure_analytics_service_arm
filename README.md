# azure_analytics_service_arm
azure arm template to deploy a simple azure analytics service server

### Create an Azure Analysis Services server

| Artifact | Description |
| ------ | ------ |
| azuredeploy.json | Azure ARM template for provisioning a Azure Analysis Services server with custome user inputs |
| azuredeploy.parameters.json | Archive of the Desired State Configuration (DSC) scripts |
| metadata.json | Metadata for the deployment |

### User Inputs

| User Inputs | Description |
| ------ | ------ |
|serverName|Name of the server to deploy|
|location|Region of deployment|
|firewallName|Name the firewall under which this server will be deployed|
|rangeStart|A range of the ip addresses to be allowed, mention the starting ip|
|rangeEnd|A range of the ip addresses to be allowed, mention the ending ip|


### Usage
#### Deploy
New-AzResourceGroupDeployment -Name <name of your deployment> -ResourceGroupName <resourcegroupname> -TemplateFile.\azuredeploy.json -TemplateParameterFile .\azuredeploy.parameters.json

#### Remove
Remove-AzResourceGroupDeployment -name <name of your deployment> -ResourceGroupName <resourcegroupname>
