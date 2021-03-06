{{{
"title": "Getting Started with SoftNAS Cloud File Gateway - Partner Template",
"date": "5-31-2015",
"author": "Bob Stolzberg",
"attachments": [],
"contentIsHTML": false
}}}

###Logo
![SoftNAS logo](https://www.softnas.com/wp/wp-content/uploads/2014/05/200x37.png)

### Partner Profile
SoftNAS, LLC is a leading storage software company that provides Simply Powerful� agile storage software that protects business data in the cloud.

SoftNAS is the #1 best-selling NAS in the cloud and believes that storage can be both powerful and frictionless, providing customers with the enterprise-grade, software-defined NAS storage required to safely and reliably operate business-critical IT systems and applications in the cloud.

[http://www.softnas.com](http://www.softnas.com)

### Contact SoftNAS

#### SoftNAS Sales and Support:
- Support Email: [support@softnas.com](mailto:support@softnas.com)
- Support Phone: 1-888-801-7524, Option 4. 
- Support Web: [https://www.softnas.com/wp/support/](https://www.softnas.com/wp/support/)
- Sales Email: [sales@softnas.com](mailto:sales@softnas.com)
- Sales Phone: 1-888-801-7524, Option 1

### Description

SoftNAS has integrated their Cloud File Gateway and NAS technology with the CenturyLink Cloud platform, publishing their virtual appliance as a CenturyLink Cloud Partner Template.  The purpose of this KB article is to help the reader take advantage of this integration to achieve rapid time-to-value for this encryption solution.

For more information including whitepapers and data sheets, please view the product information and documentation on [SoftNAS website](https://www.softnas.com/wp/support/documentation/).


### Solution Overview

SoftNAS Cloud is an enterprise-grade, full-featured cloud NAS filer and cloud storage gateway. Safely migrate business-critical applications to the CenturyLink Cloud without a physical storage appliance. Quick and easy to deploy, any IT professional can install and configure SoftNAS in minutes without specialized training. High-availability is included at no extra cost for CenturyLink Cloud users who deploy the two requisite instances. 

SoftNAS Cloud runs as a Linux-based, 64-bit CentOS redistribution guest OS, treated as a VM in a virtual server environment. In many use cases, storage devices are attached to the physical hardware layer, then presented to SoftNAS Cloud as a VM running Linux.

SoftNAS Cloud operates on an industry-standard Linux platform, and uses a derivative of the Zettabyte File System� (ZFS). This makes SoftNAS Cloud able to leverage many ZFS features and add layers of functionality for NAS solutions in virtual computing and cloud computing.

An Apache webserver provides robust, secure access along with Secure Shell (SSH). Storage is accessible via TCP/IP protocols including NFS v3, NFS v4, SMB/CIFS (Microsoft Windows File Shares), and iSCSI.

SoftNAS Cloud is packaged with a primary administration interface called SoftNAS StorageCenter�, which provides commercial-grade storage administration and management functionalities for businesses of all sizes.

#### Key Features: 

- NFS, CIFS and iSCSI support
- Connects to popular Cloud Storage services
- 99.999% reliability with cross-zone high-availability with SNAP HA(tm)
- Cross-region block replication with SnapReplicate(tm)
- Active Directory integration
- Compression, deduplication, thin-provisioning
- Easy set-up and configuration wizards, intuitive admin interface (StorageCenter)

### Offer
SoftNAS Cloud File Gateway is now available for CenturyLink Cloud Users to deploy to their account.  The SoftNAS appliance comes with a free trial that let's you use up to 100GB without having to purchase a license.  In order to purchase a license or entitlement, please visit [http://www.softnas.com/pricing](http://www.softnas.com/pricing) or contact [sales@softnas.com](mailto:sales@softnas.com)

### Audience
CenturyLink Cloud Users, Storage Administrators, IT Managers

### Impact
After reading this article, the user should feel comfortable deploying the SoftNAS Cloud File Gateway technology on CenturyLink Cloud.  SoftNAS has provided a Virtual Appliance, what CenturyLink Cloud calls a Partner Template, that can be deployed to your CenturyLink Cloud account via a Service Task.  

This deployment process for Partner Templates currently requires manual interaction via the Service Task process, but will be further automated in future releases of the CenturyLink Cloud Platform.

### Prerequisite
- Access to the CenturyLink Cloud platform as an authorized user.
- Identify a Network VLAN you want the SoftNAS instance/s to reside on

### Postrequisite
1.  Add storage to the SoftNAS VM by using Control
  1. Navigate to the SoftNAS server
  2. Click on Edit Storage button
  3. Add a Raw Partition and size appropriately
  4. Click the Save button
  5. Wait for the storage to be added

2. If you want to access your VM over the internet, please perform the following tasks once you receive an email confirming you Blueprint completed successfully:

  1. Add a [Public IP](../Network/how-to-add-public-ip-to-virtual-machine.md) to your server through Control Portal. Alternatively, you can [setup a VPN using OpenVPN](../Network/how-to-configure-client-vpn.md) or similar technology.

2. [Allow incoming traffic](../Network/how-to-add-public-ip-to-virtual-machine.md) for ports below:
  - For administrative access and use, open the following ports:
  * TCP Ports: 443
  * UDP Ports: 1
  * ICMP: All

  - For CIFS Sharing, open the following ports:
  * TCP 137, 138, 139, 445
  * TCP 389 for Active Directory
  * TCP 445 for NetBIOS Post-Windows 2000 (CIFS)
  * TCP 901 for SWAT

  - For NFS Sharing, open the following ports:
  * TCP 111, 2010-2014, 2049
  * UDP 111, 2010-2014, 2049

  - For iSCSI Sharing, open the following ports:
  * TCP 3260

### Detailed Steps to Deploy SoftNAS partner template 
SoftNAS deploys in a virtual appliance model, as a CenturyLink Cloud *Partner Template*.  Follow these step by step instructions to deploy a SoftNAS solution in to your CenturyLink Cloud account:  

1. Open a service task request ticket via email to ServiceTasks@Tier3.com with the following details.  You will need to edit some of the information below.
----
>TO: ServiceTasks@Tier3.com
>
EMAIL SUBJECT:   Ecosystem Partner Template Import Request
>
CLC Support Team,
Please create a ticket to import the Ecosystem Partner Template image referenced below to my CenturyLink Cloud Account:
- Import CenturyLink Ecosystem Partner Source Image: SoftNAS OVA
- My CenturyLink Cloud Account Alias: #### your alias
- Data Center to import image to: ### name of data center
- Server Name to import image as: ########## A unique name for the server
- VLAN in the account to add the Server to: ######## specify a VLAN 

- Additional Notes or work to be done: IMPORTANT: Please make sure that the private IP shows up in Control so that we can add a Public IP through the Portal later on if desired.
>
Please let me know if you have any questions or issues. Kindly send me a reply once the work has been completed and let us know the IP address of the server where this technology has been deployed.
>
Thank you very much,
>
Your_Name_ and_ Contact_Info_Here

-----

If you are interested in seeing this type of Partner Template deployment as an automated feature in the future, please share your input with us at [features@centurylinkcloud.com](mailto:features@centurylinkcloud.com)

### Accessing your SoftNAS appliance
1. Access your SoftNAS Gateway appliance by connecting to the server via web browser over https, e.g. https://youripaddress/

2. Follow the on-screen instructions to accept the SoftNAS user agreements and proceed to using the service. Documentation is available within the application, as well as a helpful checklist to get started.

For more information on how to use the SoftNAS solution, please visit: http://www.softnas.com/support/

### Pricing
The costs associated with this deployment is $390 one-time fee in accordance with the CenturyLink Cloud Service Tasks.  There are no SoftNAS license costs or additional fees bundled in.  Service Task Fees information is [available here](http://www.centurylinkcloud.com/service-tasks).

### Frequently Asked Questions

#### Where do I obtain my SoftNAS License or entitlements?
Existing CenturyLink Enterprise Customers can contact their Account Representative for help obtaining a SoftNAS license, or contact SoftNAS directly:
- Contact SoftNAS Sales via Email: sales@softnas.com
- Contact SoftNAS Sales via Phone: 1-888-801-7524, Option 1

#### Who should I contact for support?
* For issues related to accessing the SoftNAS partner template, setup of devices, volumes, pools or high availability, or for any licensing concerns, please visit the SoftNAS Support Website: http://www.SoftNAS.com/support
* For issues related to the initial deployment of the SoftNAS virtual appliance, cloud infrastructure (VM�s, network, storage, etc), please open a ticket using the CenturyLink Cloud Support Process.
