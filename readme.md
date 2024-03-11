# Tasks-Repository
author: Benji Kovacevic

This is sample playbook demonstrating how to create Attack Distruption scenario using Logic Apps.

# Prerequisites
1. Create App Registration in Entra ID portal and save Tenant ID, Application ID
2. Create and save Secret for App Registration (Note: We always suggest to use Azure Key Vault to save a secret to.)
3. Assign AdvancedHunting.Read.All permission to created App Registration (APIs my organization uses -> Microsoft Threat Protection)
4. Save Object ID of SOC group from Entra ID
5. Create Pan OS API key

# Quick Deployment - needs to be updated
Deploy a playbook<br>
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FTools%2FTasks-Repository%2Fazuredeploynmi.json)
[![Deploy to Azure Gov](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazuregov.png)](https://portal.azure.us/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2FAzure-Sentinel%2Fmaster%2FTools%2FTasks-Repository%2Fazuredeploynmi.json)

# Post-deployment
1. Authorize Microsft Defender for Endpoint, Entra ID, and Microsoft Outlook connections

# Note
You can update Hunting query used in Parameters section of Logic App. Please note that you will need to update action Parse JSON with new schema based on Hunting query result, as well as values used from Parse JSON action in the rest of the Logic App. 
