<h1>Cloud-Based SIEM & Honeypot SOC using Microsoft Sentinel</h1>


<h2>Project Description</h2>
In this project, I built a cloud-based Security Operations Center (SOC) and SIEM environment using Microsoft Azure and Microsoft Sentinel to simulate real-world attack monitoring and threat detection. I created a virtual environment in Azure designed to attract and monitor malicious login attempts from the public internet. Security logs from the system were centralized and analyzed using Microsoft Sentinel and KQL queries to identify attacker activity and geolocate the source of attacks.
<br />


<h2>Tools Used</h2>

- <b>Microsoft Azure</b> 
- <b>Microsoft Sentinel</b>
- <b>Azure Log Analytics Workspace</b>
- <b>Azure Virtual Network</b>
- <b>Azure Virtual Machine</b>
- <b>Azure monitoring Agent</b>
- <b>Kusto Query Language (KQL)</b>
- <b>Azure Tenant / Azure Active Directory</b>
- <b>Azure Resource Group</b>



<h2>Environments Used </h2>

- <b>Microsoft Azure (Cloud Platform)</b>
- <b>Windows 10 Virtual Machine (Target System)</b>
- <b>Public Internet (Simulated Threat Environment)</b>



<h2>Project walk-through:</h2>

<p align="center">
Created an Azure tenant and resource group to centrally manage cloud resources and enforce logical organization: <br/>
<img src="https://i.imgur.com/j4jd1Ws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
