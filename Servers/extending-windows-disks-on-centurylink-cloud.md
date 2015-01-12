{{{
  "title": "Extending Windows Disks on CenturyLink Cloud",
  "date": "10-30-2014",
  "author": "Chris Little",
  "attachments": []
}}}

<h3><strong>Overview</strong></h3>
<p>The CenturyLink Cloud platform provides a simple, self-service action to extend existing Windows Disks as storage utilization grows on Virtual Servers. &nbsp;By leveraging the Control Portal automation customers can easily, via a single click, expand
  disk sizes up to the <a href="https://t3n.zendesk.com/entries/21819996-Cloud-Server-Instance-Size-and-Performance" target="_blank">platform maximums</a>.</p>
<h3>Audience</h3>
<ul>
  <li>CenturyLink Cloud Users</li>
</ul>
<h3>Prerequisites</h3>
<ul>
  <li>Windows 2008 or Windows 2012 Operating System</li>
  <li>The administrator password stored in the Control Portal (Administrative Credentials) must match the Operating System administrator password for automated diskpart functions.</li>
</ul>
<h3>Exceptions</h3>
<ul>
  <li>Legacy Windows 2003 Operating Systems require the use of extpart or other 3rd party tools to extend partitions. &nbsp;Customers are responsible for extending partitions in the Operating System for Windows 2003 and downloading the proper tools to accomplish
    this task.</li>
  <li>The Control Portal does not permit reductions in drive sizes</li>
</ul>
<h3>Steps</h3>
<p>1. &nbsp;Navigate to the Virtual Server in the Server menu. &nbsp;The Server UI will detail the current disk sizes and driver letters assigned to the Virtual Server. &nbsp;Quick Tip: &nbsp;Make note of the Disk ID and the Partition Path you want to extend.
  &nbsp;</p>
<p><img src="https://t3n.zendesk.com/attachments/token/X7Vm3QgyZyoldxTq9ZYnvfaNO/?name=01.png" alt="01.png" />
</p>
<p><img src="https://t3n.zendesk.com/attachments/token/U2Z36FlpgRQUFhA1SItMwU70v/?name=02.png" alt="02.png" />
</p>
<p>2. &nbsp;Select the <strong>Edit Storage</strong>&nbsp;button to open the Edit Storage Dialog box. &nbsp;Input or change the slider on the appropriate Disk ID to the new drive size desired, and select apply. &nbsp;Extending of storage can be performed
  on Operating System and Data Disks. &nbsp;</p>
<p><img src="https://t3n.zendesk.com/attachments/token/Lnr1JNljYuguBV9pgIwzHpFk1/?name=03.png" alt="03.png" />
</p>
<p>3. &nbsp;Check the Queue for job completion and login to your Virtual Server to validate the drive extensions have completed successfully.</p>