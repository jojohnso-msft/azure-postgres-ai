### azure-postgres-ai-samples
# LangChain Integration Project Part 1

## Azure account requirements
To deploy and run this example, you'll need:  
•	Azure account. If you're new to Azure, [get an Azure account for free](https://azure.microsoft.com/free/cognitive-search/) and you'll get some free Azure credits to get started. [See guide to deploying with the free trial.](https://azure.microsoft.com/en-us/free/)  
•	Azure subscription with access enabled for the Azure OpenAI service. You can request access with [this form](https://aka.ms/oaiapply).     
•	Azure Database for PostgreSQL Flexible Server instance running PG 14 or higher.  
    [Quickstart: Create with Azure portal - Azure Database for PostgreSQL - Flexible Server | Microsoft Learn](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/quickstart-create-server-portal)  

## Local machine requirements
•	Install [Visual Studio Code](https://code.visualstudio.com/download)  
•	Install the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)    
•	Install [Python 3.11.x](https://www.python.org/downloads/)    
•	Install the latest available version of [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli-windows?tabs=powershell)  
•	Review the [Quickstart: Create with Azure libraries (SDK) for Python - Azure Database for PostgreSQL - Flexible Server | Microsoft Learn](https://learn.microsoft.com/en-us/azure/postgresql/flexible-server/quickstart-create-server-portal)

## Troubleshooting
Here are the most common failure scenarios and solutions:
1.	The subscription (AZURE_SUBSCRIPTION_ID) doesn't have access to the Azure OpenAI service. Please ensure AZURE_SUBSCRIPTION_ID matches the ID specified in the [OpenAI access request process.](https://aka.ms/oai/access)  
2.	You're attempting to create resources in regions not enabled for Azure OpenAI (e.g. East US 2 instead of East US), or where the model you're trying to use isn't enabled. See this [matrix of model availability.](https://aka.ms/oai/models)  
3.	You've exceeded a quota, most often number of resources per region. See [this article on quotas and limits.](https://aka.ms/oai/quotas)  
4.	You're getting "same resource name not allowed" conflicts. That's likely because you've run the sample multiple times and deleted the resources you've been creating each time, but are forgetting to purge them. Azure keeps resources for 48 hours unless you purge from soft delete. See [this article on purging resources.](https://learn.microsoft.com/azure/cognitive-services/manage-resources?tabs=azure-portal#purge-a-deleted-resource)  
5.	Windows error message when using “pip install langchain”. Python environment variable is unavailable/undefined.
  Correct this by,  
   ..1.	 using "!py -m pip install langchain"  
   ..2.	 updating your PATH  
   ..3.	 using a Python virtual environment in VS Code.

   # Azure Resources

## Azure Database for Postgres Docs  
http://aka.ms/postgresdocs

## Azure Database for Postgres Blog  
https://aka.ms/azurepostgresblog

## Azure Postgres Feedback Forum  
https://aka.ms/pgfeedback

## Ask Questions  
AskAzureDBforPostgreSQL@service.microsoft.com
