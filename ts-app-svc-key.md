---

copyright: 
  years: 2014, 2021
lastupdated: "2021-10-21"

keywords: kubernetes, iks

subcollection: containers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}


# Why does binding a service to a cluster results in service does not support service keys error?
{: #ts-app-svc-key}

**Infrastructure provider**:
* ![Classic infrastructure provider icon.](images/icon-classic-2.svg) Classic
* ![VPC infrastructure provider icon.](images/icon-vpc-2.svg) VPC


When you run `ibmcloud ks cluster service bind --cluster <cluster_name> --namespace <namespace> --service <service_instance_name>`, you see the following message.
{: tsSymptoms}

```sh
This service doesn't support creation of keys
```
{: screen}



Some services in {{site.data.keyword.cloud_notm}}, such as {{site.data.keyword.keymanagementservicelong}} do not support the creation of service credentials, also referred to as service keys. Without the support of service keys, the service is not bindable to a cluster. To find a list of services that support the creation of service keys, see [Enabling external apps to use {{site.data.keyword.cloud_notm}} services](/docs/account?topic=account-externalapp#externalapp).
{: tsCauses}



To integrate services that do not support service keys, check if the service provides an API that you can use to access the service directly from your app. For example, if you want to use {{site.data.keyword.keymanagementservicelong}}, see the [API reference](https://cloud.ibm.com/apidocs/key-protect){: external}.
{: tsResolve}








