# Windows_2008_DB_Cluster_Creation
<h1> Configuring Windows & DB Cluster on Windows 2008 R2 & SQL 2008 R2 <h1>
  <img src=/"Active_Passive_Cluster.jpg">
<h2>1. Creating cluster nodes</h2>
<ol>
  <li> Installation of OS - Windows Enterprise Edition 2008 R2 </li>
<li> Assiging IP & DNS Server Addresses to both Node-1 & Node-2</li>
<li> Changing Computer Names</li>
&nbsp;&nbsp;&nbsp;&nbsp;node-1<br>
&nbsp;&nbsp;&nbsp;&nbsp;node-2
<li>d. Copying\Downloading installer on both nodes</li>
</ol>

<h2>2. Creating Domain Controller</h2>
<ol>
<li> Installation of OS - Window Standard \ Enterprise 2008 R2</li>
<li> Assiging IP & DNS Server Addresses to Domain Controller</li>
<li> Installing AD Domain Service (dcpromo)</li>
&nbsp;&nbsp;&nbsp;&nbsp;Adding Forest Root Domain<br>
&nbsp;&nbsp;&nbsp;&nbsp;Adding IP to Reserver Lookup Zone<br>
&nbsp;&nbsp;&nbsp;&nbsp;Creating new Host(defining IP Addresses) for Domain Controller<br>
<li> Installing iSCASI drives by Adding Drives from Node 1 & Node 2</li>
<li> Adding Quorum drive </li>
<li> Adding nodes to Domain</li>
<li> Disabling firewall</li>
<li> Validating disk setup using Disk Management</li>
</ol>

<h2>3. Creating Failover Windows Cluster</h2>
<ol>
<li> Adding Windows Failover Cluster on both nodes</li>
&nbsp;&nbsp;&nbsp;&nbsp;Add cluster server name<br>
&nbsp;&nbsp;&nbsp;&nbsp;Cluster failover pre-checks<br>
&nbsp;&nbsp;&nbsp;&nbsp;Cluster failover validation<br>
&nbsp;&nbsp;&nbsp;&nbsp;Viewing Report<br>
<li> Assiging Cluster Name & IP</li>
<li> Disabling firewall</li>
</ol>

<h2>4. Configuring Active\Passive SQL Cluster On Node-1 & Node-2 </h2>
<ol>
<li> adding .Net Extensibility features</li>
<li> New SQL Server failover cluster installation </li>
&nbsp;&nbsp;&nbsp;&nbsp;DB Engine<br>
&nbsp;&nbsp;&nbsp;&nbsp;MS SQL Client<br>
&nbsp;&nbsp;&nbsp;&nbsp;Management Tools<br>
&nbsp;&nbsp;&nbsp;&nbsp;Clients Tools Connectivity<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SQL Server Cluster Name (gogate)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SQL Server Instance Name (dgogate)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Specifying IP Addresses<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Create domain account for SQL<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Make Admin in both Nodes adding in Admin Group<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Use domin account user id & password for DB Services<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Use mixed mode authentication <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Add users as Admins<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Install <br>
</ol>

<h2>5. Configuring Active\Passive SQL Cluster On Node-2 </h2>
<ol>
<li> adding .Net Extensibility features</li>
<li> Add node to failover cluster </li>
&nbsp;&nbsp;&nbsp;&nbsp;SQL Server Cluster Name (gogate)<br>
&nbsp;&nbsp;&nbsp;&nbsp;SQL Server Instance Name (mgogate)<br>
&nbsp;&nbsp;&nbsp;&nbsp;Use domin account user id & password for DB Services<br>
&nbsp;&nbsp;&nbsp;&nbsp;Use mixed mode authentication <br>
<li> Validation of DB Cluster</li>
Creating new DB
</ol>
