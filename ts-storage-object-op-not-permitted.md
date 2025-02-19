---

copyright: 
  years: 2014, 2021
lastupdated: "2021-10-21"

keywords: kubernetes, iks, help, network, connectivity

subcollection: containers

content-type: troubleshoot

---


{{site.data.keyword.attribute-definition-list}}


# Why does my app pod fail with an `Operation not permitted` error?
{: #cos_operation_not_permitted}

**Infrastructure provider**:
* ![Classic infrastructure provider icon.](images/icon-classic-2.svg) Classic
* ![VPC infrastructure provider icon.](images/icon-vpc-2.svg) VPC


When you create a PVC, you see an error message similar to the following:
{: tsSymptoms}

```sh
EPERM: operation not permitted
```
{: screen}


IAM has introduced a `refresh_token_expiration` key which causes an issue with the IAM credential response parser, where the parser was not able to differentiate between `expiration` and `refresh_token_expiration`.
{: tsCauses}

This issue is resolved in the [community repo](https://github.com/s3fs-fuse/s3fs-fuse/pull/1421) and in the {{site.data.keyword.cos_full_notm}} plug-in.


Complete the steps to [update your {{site.data.keyword.cos_full_notm}} plug-in to the latest version](/docs/containers?topic=containers-object_storage#update_cos_plugin).
{: tsResolve}






