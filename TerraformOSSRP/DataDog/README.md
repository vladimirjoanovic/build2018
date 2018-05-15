# Deploying a Datadog dashboard using the ARM TerraformOSS RP

Datadog provides an Azure VM Extension to enable Azure customers to capture metrics from their VMs and make them available to Datadog's services. The ARM TerrafomOSS RP provides access to the Datadog TF provider which means that it is now possible to configure a Dashboard in the Datadog SaaS application to visualise this data in the same template that deploys a VM and the Datadog VM extension . This template creates a VM , installs the Datadog VM Extension and then sets up a timeboard in Datadog using the TerraformOSS RP.

## Pre-requisites

The Azure Subscription used to deploy the template must be enabled for the Microsoft.TerrformOSS RP. This demo requires a datadog account, a free trial account can be created at https://www.datadoghq.com/ 

Once the account is setup navigate to https://app.datadoghq.com/account/settings#api and create a new API Key.

## Deploy the template

Use the values for the API Key and the Application Key as parameters to the template, you also need to provide a password for the VM. The template will create a VM, install the Datadog VM extension and then create a new Datadog dashboard, once the template has been successfully deployed the new dashboard will be visible at https://app.datadoghq.com/dashboard/lists
