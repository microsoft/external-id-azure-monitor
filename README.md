# Microsoft Entra External ID External Tenant Reports

In this repo, you will find samples to create your own dashboard, reports & alerts based on your external tenant logs. 

## Security

See a security issue with some contents of this repo?

**Please do not report security vulnerabilities through public GitHub issues.**

## Getting Started

- Read about [Audit Logs](https://docs.microsoft.com/en-us/azure/active-directory-b2c/view-audit-logs) and [Sign in Logs](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/reference-azure-monitor-sign-ins-log-schema) to gain better understanding about their usage and schema.

- Read about [Azure Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/overview) to understand its key features.

- Read about [Azure Active Directory reporting latencies](https://docs.microsoft.com/en-us/azure/active-directory/reports-monitoring/reference-reports-latencies) and [Log data ingestion time in Azure Monitor](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-ingestion-time) which covers various latencies across Azure External ID and Azure Monitor.

- Read about [Log Analytics Queries](https://docs.microsoft.com/en-us/azure/azure-monitor/log-query/get-started-portal) to understand how to create and run reports using [Kusto](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/concepts/) language.

- Read about [Azure Monitor Workbooks](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/workbooks-overview) which provides a flexible canvas for data analysis and the creation of rich visual reports.

- Read about [Azure Alerts](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/alerts-overview) their benefits and usage patterns.

## Prerequisites

- You will be required to create a Microsoft Entra External ID external tenant, see the guidance [here](https://learn.microsoft.com/en-us/entra/external-id/customers/quickstart-tenant-setup).

- To use the sample artifacts in this repo, follow the instructions described in the [Monitor External ID with Azure Monitor](https://learn.microsoft.com/en-us/entra/external-id/customers/how-to-azure-monitor) to setup Azure Monitor and route sign-in and auditing logs to Log Analytics workspace. After the setup is complete, it may take up to 45 minutes or so for logs to show up in Log Analytics workspace. Subsequently, Azure monitor will sync the logs within few minutes as they get generated in your external tenant. 
    
    <a href=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fexternal-id-azure-monitor%2Fmain%2Ftemplates%2FrgDelegatedResourceManagement.json data-linktype="external"><img src=https://aka.ms/deploytoazurebutton alt="Deploy to Azure" data-linktype="external"></a>

## Workbooks

All the reports in this repo are based on [Azure Monitor Workbooks](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/workbooks-overview) which provide a flexible canvas for data analysis and the creation of rich visual reports within the Azure portal or Entra admin center.

### Deploy workbooks via ARM template

| Name      | Workbook Id | Deploy |
| --------- | ------------| ------ |
| Authentications Workbook      |d284045e-b1c1-4d82-a8b8-b1a59a98eb33|<a href=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fexternal-id-azure-monitor%2Fmain%2Ftemplates%2FauthenticationsWorkbookDeployment.json data-linktype="external"><img src=https://aka.ms/deploytoazurebutton alt="Deploy to Azure" data-linktype="external"></a>    |
| MFA Overview and MFA Failures Workbook      |f405c652-7c08-47b9-8005-dc33ae331748|<a href=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fexternal-id-azure-monitor%2Fmain%2Ftemplates%2FmfaWorkbookDeployment.json data-linktype="external"><img src=https://aka.ms/deploytoazurebutton alt="Deploy to Azure" data-linktype="external"></a>    |
| User Behaviour Workbook      |65bf1d28-2dc8-4099-8cb1-e3f4a2f32256|<a href=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fexternal-id-azure-monitor%2Fmain%2Ftemplates%2FuserBehaviourWorkbookDeployment.json data-linktype="external"><img src=https://aka.ms/deploytoazurebutton alt="Deploy to Azure" data-linktype="external"></a>    |
| Risk Detection Workbook      |0d8084bd-cc7d-4670-988a-ee9553a19fa2|<a href=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fexternal-id-azure-monitor%2Fmain%2Ftemplates%2FriskDetectionWorkbookDeployment.json data-linktype="external"><img src=https://aka.ms/deploytoazurebutton alt="Deploy to Azure" data-linktype="external"></a>    |
| Conditional Access Workbook      |a9f52ac8-7a5d-4f86-86b8-092a74410758|<a href=https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmicrosoft%2Fexternal-id-azure-monitor%2Fmain%2Ftemplates%2FconditionalAccessWorkbookDeployment.json data-linktype="external"><img src=https://aka.ms/deploytoazurebutton alt="Deploy to Azure" data-linktype="external"></a>    |

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
