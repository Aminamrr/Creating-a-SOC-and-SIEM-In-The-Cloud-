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
Configured a Virtual Network (VNet) and subnet to establish the internal network architecture:  <br/>
<img src="https://i.imgur.com/1YUFqlV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Deployed a Windows virtual machine to act as the target system (honeypot) for capturing malicious activity: <br/>
<img src="https://i.imgur.com/TKVNxs0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configured Network Security Groups (NSG) and disabled local firewall protections to allow unrestricted inbound traffic, intentionally exposing the system to the public internet to attract brute-force attacks:  <br/>
<img src="https://i.imgur.com/LUObGKo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created a Log Analytics Workspace and configured the Azure Monitoring Agent to forward Windows security event logs from the VM:  <br/>
<img src="https://i.imgur.com/c6cNrut.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 <img src="https://i.imgur.com/KGVvT8B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Deployed Microsoft Sentinel and connected it to the Log Analytics Workspace to enable centralized log analysis and threat detection:  <br/>
<img src="https://i.imgur.com/h27PnpZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Imported a watchlist containing IP geolocation data and correlated attacker IP addresses with geographic information:  <br/>
<img src="https://i.imgur.com/vOWwtmN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Used Kusto Query Language (KQL) to query Event ID 4625 logs and identify failed RDP login attempts, indicating potential brute-force attacks. This query filters Windows Security Events for failed logon attempts (Event ID 4625) and enriches the data by correlating attacker IP addresses with a geolocation watchlist. Using the ipv4_lookup function, it maps IP addresses to geographic data, enabling identification and visualization of attack origins for threat analysis:  <br/>
<img src="https://i.imgur.com/LkOwIQd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Built a Sentinel workbook to visualize geolocated failed login attempts, providing a global view of attack activity. This enabled identification of attack trends, clustering of malicious IP addresses, and insight into the geographic origin of brute-force attempts targeting the exposed virtual machine:  <br/>
<img src="https://i.imgur.com/STOXMpD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
