---

copyright: 
  years: 2014, 2021
lastupdated: "2021-10-21"

keywords: kubernetes, iks, help, network, connectivity

subcollection: containers

content-type: troubleshoot

---


{{site.data.keyword.attribute-definition-list}}


# Why can't my PVC access an existing bucket?
{: #cos_access_bucket_fails}

**Infrastructure provider**:
* ![Classic infrastructure provider icon.](images/icon-classic-2.svg) Classic
* ![VPC infrastructure provider icon.](images/icon-vpc-2.svg) VPC




When you create the PVC, the bucket in {{site.data.keyword.cos_full_notm}} cannot be accessed. You see an error message similar to the following:
{: tsSymptoms}

```sh
Failed to provision volume with StorageClass "ibmc-s3fs-standard-regional": pvc:1b2345678b69175abc98y873e2:cannot access bucket <bucket_name>: NotFound: Not Found
```
{: screen}


You might have used the wrong storage class to access your existing bucket, or you tried to access a bucket that you did not create. You cannot access a bucket that you did not create.
{: tsCauses}


Verify your bucket details and storage class and recreate your PVC.
{: tsResolve}

1. From the [{{site.data.keyword.cloud_notm}} dashboard](https://cloud.ibm.com/){: external}, select your {{site.data.keyword.cos_full_notm}} service instance.
2. Select **Buckets**.
3. Review the **Class** and **Location** information for your existing bucket.
4. Choose the appropriate [storage class](/docs/containers?topic=containers-object_storage#cos_storageclass_reference).
5. Make sure that you provide the correct name of your existing bucket.






