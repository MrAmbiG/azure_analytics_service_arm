# azure_analytics_service_arm
azure arm template to deploy a simple azure analytics service server


### Usage
#### Deploy
New-AzResourceGroupDeployment -Name <name of your deployment> -ResourceGroupName <resourcegroupname> -TemplateFile.\azuredeploy.json -TemplateParameterFile .\azuredeploy.parameters.json

#### Remove
Remove-AzResourceGroupDeployment -name <name of your deployment> -ResourceGroupName <resourcegroupname>
