# Attack-Maps-and-Log-Visualizations
## **World Map Visualization Scenarios**  
The goal is to create world map visualization workbooks, likely using Microsoft Sentinel Workbooks, a Security Information and Event Management (SIEM) tool, 
to display the geographical origins of various activities based on the source IP address.

Here's a breakdown of the scenarios and what each visualization will show:

| Scenario | Data Source/Log Type | Key Metric/Focus | What the Map Will Show |
| :---- | :---- | :---- | :---- |
| **[Entra ID (Azure) Authentication Success](https://github.com/jacobvasquez92/Attack-Maps-and-Log-Visualizations/blob/main/Entrada%20ID%20(Azure)%20Authentication%20Success.md)** | Azure Active Directory (Entra ID) Sign-in Logs | Successful Logins | Geographical spread of **successful user access** to cloud resources. This helps establish a baseline for legitimate access. |
| **Entra ID (Azure) Authentication Failures** | Azure Active Directory (Entra ID) Sign-in Logs | Failed Logins | Geographical spread of **unsuccessful attempts** to access cloud resources. High volume from specific regions can indicate brute-force or credential-stuffing attacks. |
| **Azure Resource Creation** | Azure Activity Logs (Resource Provider Operations) | Resource Deployment Events | Locations from which **new Azure resources** (VMs, storage accounts, etc.) are being provisioned. This is key for tracking administrative activity and identifying suspicious, non-admin resource deployments. |
| **VM Authentication Failures** | VM/Operating System Audit Logs (e.g., Windows Event Logs, Linux auth.log) | Failed VM Logins | Geographical spread of **failed authentication attempts against Virtual Machines** (RDP, SSH, etc.). This often highlights automated scanning and brute-force attempts targeting on-prem or IaaS assets. |
| **Malicious Traffic Entering the Network** | Firewall/Network Security Group (NSG) Logs, Intrusion Detection/Prevention System (IDS/IPS) Logs | Denied or Alerted Traffic | **Geographical origin of known malicious traffic**, often based on threat intelligence feeds matched against the source IP. This provides a direct visualization of incoming threats. |

