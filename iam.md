---

copyright:
  years: 2020
lastupdated: "2020-10-09"

keywords: IBM Cloud, Master Data Management, MDM, identity, access management, roles, actions, policies, IAM access for Master Data Management, permissions for Master Data Management, identity and access management for Master Data Management, roles for Master Data Management, actions for Master Data Management, assigning access for Master Data Management

subcollection: mdm-oc

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}

# Managing access for {{site.data.keyword.mdm-oc_full_notm}}
{: #iam}

Access to {{site.data.keyword.mdm-oc_full}} service instances for users in your account is controlled by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Every user that accesses the {{site.data.keyword.mdm-oc_full_notm}} service in your account must be assigned an access policy with an IAM role defined. The policy determines what actions a user can perform within the context of the service or instance that you select. The allowable actions are customized and defined by the {{site.data.keyword.Bluemix_notm}} service as operations that are allowed to be performed on the service. The actions are then mapped to IAM user roles.

Policies enable access to be granted at different levels. Some of the options include the following: 

* Access across all instances of the service in your account.
* Access to an individual service instance in your account. <!-- if this applies -->
* Access to a specific resource within an instance. <!-- if this applies list what resoureceType attributes are supported -->

After you define the scope of the access policy, you assign a role, which determines the user's level of access. Review the following tables that outline what actions each role allows within the {{site.data.keyword.mdm-oc_full_notm}} service.

The following table details actions that are mapped to platform management roles. Platform management roles enable users to perform tasks on service resources at the platform level, for example, assign user access for the service, create or delete instances, and bind instances to applications.

| Platform role | Description of actions | 
|--------------------------|------------------------|
| Viewer                   | As a viewer, you can view service instances, but you can't modify them. This platform role is automatically assigned the 'Reader' service access role. |
| Editor                   | As an editor, you can perform all platform actions except for managing the account and assigning access policies. This platform role is automatically assigned the 'Reader' service access role.           |
| Operator                 | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. This platform role is automatically assigned the 'Reader' service access role.           | 
| Administrator            | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. This platform role is automatically assigned the 'Manager' service access role. |
{: row-headers}
{: caption="Table 1. IAM platform roles and actions" caption-side="top"}
{: summary="The rows are read from left to right. The first column is the platform management role. The second column is a description of the actions in the service that the platform management role permits."}

The following table details actions that are mapped to service access roles. Service access roles enable users access to {{site.data.keyword.mdm-oc_full}} microservices and provide the ability to call the {{site.data.keyword.mdm-oc_full}} APIs.

| Service role | Description of actions | 
|---------------------|------------------------|
| Data Reader              | As a Data Reader, you can perform read only actions in the Data microservice.            | 
| Data Writer              | As a Data Writer, you can perform read and write actions in the Data microservice |
| Data Manager            | As a Data Manager, you can perform read, write, and manage actions in the Data microservice. |
| Matching Reader            | As a Matching Reader, you can perform read actions in the Matching microservice. |
| Matching Writer            | As a Matching Writer, you can perform read and write actions in the Matching microservice. |
| Matching Manager            | As a Matching Manager, you can perform read, write, and manage actions in the Matching microservice. |
| Model Reader           | As a Model Reader, you can perform read actions in the Model microservice. |
| Model Writer            | As a Model Writer you can perform write actions in the Model microservice. |
| Model Manager           | As a Model Manager, you can perform manage actions in the Model microservice. |
| Configurator Reader            | As a Configurator Reader, you can perform read actions in the Configuration microservice. |
| Configurator Manager            | As a Configurator Manager, you can perform manage actions in the Configuration microservice. |
| Pair Analysis Reader            | As a Pair Analysis Reader, you can perform read actions in the Pair Analysis microservice. |
| Pair Analysis Writer            | As a Pair Analysis Writer, you can perform read and write actions in the Pair Analysis microservice. |
| Job Writer            | As a Job Writer, you can perform read and write actions in the Jobs microservice. |
| Job Reader            | As a Job Reader, you can perform read actions in the Jobs microservice. |
| DataSteward           | As a Data Steward, you can add or delete rules from the Matching microservice. |
{: row-headers}
{: caption="Table 2. IAM service access roles and actions" caption-side="top"}
{: summary="The rows are read from left to right. The first column is the service access role. The second column is a description of the actions in the service that the service access role permits."}

For more information about how roles within Cloud Pak for Data as a Service, see [Roles in Cloud Pak for Data as a Service](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/roles.html?audience=wdp&context=cpdaas).

For information about assigning user roles in the IBM Cloud console, see [Managing access to resources](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
