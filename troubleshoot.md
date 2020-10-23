---

copyright:
  years: 2020
lastupdated: "2020-09-30"

keywords: troubleshoot, troubleshooting, question, known issues, issue, problem, Master Data Management, MDM, IBM Cloud, Cloud  Pak for Data, Cloud Pak for Data as a Service

subcollection: mdm-oc

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note:.deprecated}
{:troubleshoot: data-hd-content-type='troubleshoot'}

<!-- You must add the troubleshoot content type in your attribute definitions AND to each troubleshoot H2. This will ensure that the troubleshoot entry is pulled into other locations, like chatbots. -->

# Troubleshooting for {{site.data.keyword.mdm-oc_full_notm}}
{: #troubleshoot}

General problems with using {{site.data.keyword.mdm-oc_full}} (Beta) might include REST API authentication issues or other API issues. In many cases, you can recover from these problems by following a few easy steps.
{:shortdesc}

## Authorization token has not been provided
{: #troubleshoot-auth-notoken}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

An authorization token has not been provided in the Authorization header.
{: tsCauses}

Pass an authorization token in the Authorization header.
{: tsResolve}

## Invalid authorization token
{: #troubleshoot-auth-invalid}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

Authorization token which has been provided cannot be decoded or parsed.
{: tsCauses}

Pass correct authorization token in the Authorization header.
{: tsResolve}

## Authorization token and instance_id which was used in the request are not the same
{: #troubleshoot-auth-nomatch}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

The Authorization token that has been used is not generated for the service instance against which it was used.
{: tsCauses}

Pass an authorization token in the Authorization header which corresponds to the service instance which is being used.
{: tsResolve}

## Authorization token is expired
{: #troubleshoot-auth-expired}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

Authorization token is expired.
{: tsCauses}

Pass an unexpired authorization token in the Authorization header.
{: tsResolve}

## Public key needed for authentication is not available
{: #troubleshoot-auth-nokey}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

This is an internal service issue.
{: tsCauses}

The issue needs to be fixed by support team.
{: tsResolve}

## Operation timed out after {{timeout}}
{: #troubleshoot-timeout}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

The timeout occurred while performing a requested operation.
{: tsCauses}

Try to invoke the desired operation again.
{: tsResolve}

## Unhandled exception of type {{type}} with {{status}}
{: #troubleshoot-unhandled-status}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

This is an internal service issue.
{: tsCauses}

Try to invoke the desired operation again. If it occurs again, then it might need to be fixed by the support team.
{: tsResolve}

## Unhandled exception of type {{type}} with {{response}}
{: #troubleshoot-unhandled-resp}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

This is an internal service issue.
{: tsCauses}

Try to invoke the desired operation again. If it occurs again, then it might need to be fixed by the support team.
{: tsResolve}

## Unhandled exception of type {{type}} with {{json}}
{: #troubleshoot-unhandled-json}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

This is an internal service issue.
{: tsCauses}

Try to invoke the desired operation again. If it occurs again, then it might need to be fixed by the support team.
{: tsResolve}

## Unhandled exception of type {{type}} with {{message}}
{: #troubleshoot-unhandled-msg}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

This is an internal service issue.
{: tsCauses}

Try to invoke the desired operation again. If it occurs again, then it might need to be fixed by the support team.
{: tsResolve}

## Requested object could not be found
{: #troubleshoot-notfound}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

The request resource could not be found.
{: tsCauses}

Ensure that you are referring to the existing resource.
{: tsResolve}

## Underlying database reported too many requests
{: #troubleshoot-maxreqs}
{: troubleshoot}

The REST API cannot be invoked successfully.
{: tsSymptoms}

The user has sent too many requests in a given amount of time.
{: tsCauses}

Try to invoke the desired operation again.
{: tsResolve}

