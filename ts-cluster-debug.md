---

copyright: 
  years: 2014, 2021
lastupdated: "2021-10-21"

keywords: kubernetes, iks

subcollection: containers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}


# Debugging clusters
{: #debug_clusters}
{: troubleshoot}
{: support}

Review the options to debug your clusters and find the root causes for failures.
{: shortdesc}

**Infrastructure provider**:
* ![Classic infrastructure provider icon.](images/icon-classic-2.svg) Classic
* ![VPC infrastructure provider icon.](images/icon-vpc-2.svg) VPC

1. List your cluster and find the `State` of the cluster.

    ```sh
    ibmcloud ks cluster ls
    ```
    {: pre}

2. Review the `State` of your cluster. If your cluster is in a **Critical**, **Delete failed**, or **Warning** state, or is stuck in the **Pending** state for a long time, start [debugging the worker nodes](/docs/containers?topic=containers-debug_worker_nodes).






