{{{
  "title": "Deploying Kerberos for Cloudera on CenturyLink Cloud",
  "date": "06-04-2015",
  "author": "John Haefele",
  "attachments": [],
  "contentIsHTML": false
}}}

##Overview

Cloudera Hadoop can be secured with Kerberos through the use of the Hadoop Kerberos addon. This walkthrough assumes you have an existing Cloudera cluster (make sure you know the **exact** name of this cluster).

###Deploy the Hadoop Kerberos addon

1\. Search for "kerberos" in the Blueprints Library. Then, click the "CLC Hadoop Kerberos addon".

![CLC Search kerberos](../images/deploying-hadoop-kerberos-addon-01.png)

2\. Click on the "Deploy Blueprint" button.

![CLC Deploy Kerberos addon Blueprint](../images/deploying-hadoop-kerberos-addon-02.png)

3\. Fill out the appropriate details for the CLC Hadoop Kerberos addon Blueprint. The Cloudera Cluster name is the name of you cluster; the Realm name is the Kerberos KDC Realm name.

![CLC Specify Cloudera Cluster/Realm names](../images/deploying-hadoop-kerberos-addon-03.png)  

>**Notes:**
- You must enter the EXACT Cloudera Cluster name in order for the Kerberos addon to deploy correctly.
- Best practice for Cluster name is no spaces
- Best practice for Realm name is all caps, no spaces

4\. Verify your configuration details.

![CLC Verify Addon Configuration](../images/deploying-hadoop-kerberos-addon-04.png)

5\. Once verified, click on the ‘deploy blueprint’ button.
You will see the deployment details along with an email stating the Blueprint is queued for execution.

![CLC Kerberos addon Blueprint Executing](../images/deploying-hadoop-kerberos-addon-05.png)

You will receive a second email reporting that the addon Blueprint has been successfully deployed. You will receive two more email messages, the first letting you know that the Kerberos configuration is begun, and a follow-up upon completion. The amount of time needed for configuration will vary depending on the size of your cluster. **_Please do not attempt to use the servers until you have received this final email._**

6\. Veryify Kerberos Addon Installation
During the Kerberos addon installation, the Cloudera Manager will create all of the menus needed for all Kerberos-enabled services.

To verify Kerberos is installed on Cloudera cluster, click on the **Administration** menu and select **Kerberos**.

![CLC Administration Menu in Cloudera Manager](../images/deploying-hadoop-kerberos-addon-06.png)

The screen will indicate whether Kerberos is enabled. You can select the **Credentials** tab to view the Kerberos setup and key that were generated.

![CLC Kerberos Details Screen](../images/deploying-hadoop-kerberos-addon-07.png)

When Kerberos is enabled, all services effected by Kerberos (e.g., mgmt1, zookeeper, hdfs, and hbase) should be running properly.

![CLC Cloudera Manager with Services Functional](../images/deploying-hadoop-kerberos-addon-08.png)

###Other Resources
- More on configuring authentication in Cloudera: [Configuring Authentication in Cloudera Manager](http://www.cloudera.com/content/cloudera/en/documentation/core/latest/topics/cm_sg_authentication.html)
- Kerberos documentation: [Kerberos: The Network Authentication Protocol](http://web.mit.edu/Kerberos/)
- Kerberos 5 Release 1.8.6 Notes: (krb5-1.8.6) [Kerberos 5 Release 1.8.6 Notes](http://web.mit.edu/Kerberos/krb5-1.8/)