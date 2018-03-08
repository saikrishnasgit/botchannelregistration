# registerbotchannel
Bot Channel Registration
 ## To create Bot Chaneel Registration
This template will be helpful to register Bot Channel.

## Bot Channel Registration:
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsaikrishnasgit%2Fbotchannelregistration%2Fmaster%2Ftemplate_botchannelregistration.json" target="_blank"><img src="http://azuredeploy.net/deploybutton.png"/>
</a>



## Deployment steps

You can click the "Deploy to Azure" button at the beginning of this document.
- Enter the Azure subscription / Resource group / Region
- Enter the Logic App name
- Enter the name / display name of Dynamics CRM connection
- Enter the name / display name of Azure Blob connection
- Enter the Azure storage account name
- Enter the Azure Storage account Access key
- Click 'I agree to the terms and conditions stated above'
- Click Purchase

## Usage

Once the deployment is completed, you can perform below steps to test your Logic App:
- Open the Logic App -> API Connections
- Open CRM API connection -> Click Authorize and save
- Run the Logic App and validate the attachments from CRM to Azure Blob
- Open Logic App in Code View -> find the text 'CRMORGUNIQUENAME_TOBE_REPLACED' and replace it with your CRM organization unique name
- Make sure the the CRM org unique name is having correct extension based on region. (Ex: NA its crm , Australia its crm6 and so on)
- Recurrence: Change the recurrence schedule of Logic App as per your requirement to make it schedule job
- Note: By default, Logic App moves top 2 attachment records ("$top": 2) to Azure Blob. Please update the Logic App in code view with the number you wanted

## Important: 
If you have Attachment Management solution installed from AppSource, please disable the RetrieveMultiple / Update plugin steps on Note & ActivityMimeAttachment entities to avoid any performance issues.
