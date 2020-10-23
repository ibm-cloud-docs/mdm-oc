---

copyright:
  years: 2020
lastupdated: "2020-10-06"

keywords: IBM Cloud, Master Data Management, MDM, authentication, API, REST

subcollection: mdm-oc

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# About the {{site.data.keyword.mdm-oc_full}} API
{: #api}

{{site.data.keyword.mdm-oc_full}} provides a powerful REST API that enables you to connect MDM's powerful master data management capabilities to your systems and processes. Use the MDM REST APIs, and the corresponding SDKs, to develop applications that interact with the service.
{: shortdesc}

For more information, including descriptions and examples for each API method, see the [API Reference documentation](https://cloud.ibm.com/apidocs/mdm).
{: note}

{{site.data.keyword.mdm-oc_full_notm}} API methods are categorized into services:
- Configuration
- Data
- Matching
- Model

## Configuration service
{: #api-config}

The Configuration service enables data engineers to configure the data model, manage project metadata, suggest mapping and matching attributes, and initiate the data matching process. 

This service supports the configuration user experience to load and manage data assets and the data model.

## Data service
{: #api-data}

The Data service enables line of business users or data analysts to search for and modify the data in the system. This service supports text searches, get records, and get entities. Its functions include create, edit, delete, and export record. 

This service supports the master data explorer user experience to search, view, edit, and export records and entities.

## Matching service
{: #api-matching}

The Matching service enables data engineers to manage the data matching process. This service is used to initiate, change, manage, and lookup the matching rules, algorithms, and metadata associated with matching. 

This service supports the configuration and master data explorer user experiences to initiate matching and to visualize matching results and master data entities.

## Model service
{: #api-model}

The Model service enables data engineers to manage the metadata in the MDM system. This service provides the ability to view and modify the model, the matching algorithm, and the composite view rules.

This service supports the configuration and master data explorer user experiences to manage and visualize the data model and composite views.
