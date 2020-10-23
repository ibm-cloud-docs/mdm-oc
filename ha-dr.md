---

copyright:
  years: 2020
lastupdated: "2020-10-09"

keywords: high availability, disaster recovery, HADR, Master Data Management, MDM, Cloud Pak for Data as a Service, HA, DR

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

# High availability and disaster recovery
{: #ha-dr}

{{site.data.keyword.mdm-oc_full}} (Beta) is highly available in the {{site.data.keyword.Bluemix_notm}} **Dallas** location. Recovering from potential disasters that affect an entire location requires planning and preparation.
{: shortdesc}

The Dallas location is considered a multizone region (MZR). For redundancy, each MZR is comprised of three or more data centers (zones) that are independent from each other to ensure that single failure events affect only a single zone. MZRs provide low latency (< 2 milliseconds latency) and high bandwidth (> 1000 Gbps) connectivity across zones. The advantage of an MZR is that it provides consistent cloud services across different zones, better resiliency, availability, and higher interconnect speed between data centers for the deployed resources. Deploying an application in an MZR rather than a single-zone region (SZR) can increase the availability from 99.9% to 99.99% when deployed over three zones. Descriptions of zones and regions are available in [the IBM Cloud documentation](https://cloud.ibm.com/docs/overview?topic=overview-locations).

You are responsible for understanding your configuration, customization, and usage of the service. You are also responsible for being ready to re-create an instance of the service and to restore your data. See [How do I ensure zero downtime?](/docs/overview?topic=overview-zero-downtime#zero-downtime) to learn more about the high availability and disaster recovery standards in {{site.data.keyword.Bluemix_notm}}. You can also find information about [Service Level Agreements](/docs/overview?topic=overview-zero-downtime#SLAs).  

## High availability

{{site.data.keyword.Bluemix_notm}} offers in-region data redundancy that enables high availability protection. IBM provides automatic data replication for client databases that contain training or custom model data at no additional cost. Replication is completed across in-region availability zones within {{site.data.keyword.Bluemix_notm}} data centers.

## Disaster recovery

Disaster recovery can become an issue if an {{site.data.keyword.Bluemix_notm}} location experiences a significant failure that includes the potential loss of data. You must wait for IBM to bring a location back online if it becomes unavailable. If underlying data services are compromised by the failure, you must also wait for IBM to restore those data services.

This service relies on the multiple zones within the Dallas region to provide resiliency. It is assumed that the impact of a disaster is limited to one zone in the region. This means that operations should be expected to continue without disruption even when one of the zones is not available. 

### In case of a single zone failure

In-region business continuity is provided through automatic replication across in-region availability zones within each {{site.data.keyword.Bluemix_notm}} data center.

### In case of a multizone failure (region is down)

This service is comprised of several components that will need to be recovered in the case of a disaster with a given data center. {{site.data.keyword.Bluemix_notm}} (Beta) is only offered in the Dallas region, so there is no cross-region replication. 
If a catastrophic failure occurs, IBM might not be able to recover data from database backups. 

### In case of data corruption

If data becomes corrupted across all tenants, IBM might need to restore from a recent backup. This restore would affect the data for all tenants.

### In case of accidental deletion or other errors that result in data loss

Services cannot differentiate between accidental deletions and intentional ones. If you accidentally delete some data from your service, IBM cannot restore it from a backup, as it would affect other tenants. In this case, it is your responsibility to add the data back into the service using either the service's API or web interface.
