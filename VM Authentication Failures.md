# VM Authentication Failures  
## What This Map Demonstrates:  
Geographical spread of failed authentication attempts against Virtual Machines (RDP, SSH, etc.). 
This often highlights automated scanning and brute-force attempts targeting on-prem or IaaS assets.  

<img width="1311" height="797" alt="image" src="https://github.com/user-attachments/assets/e191a5e8-58cf-4712-9b09-b95bde42dd61" />  

---

## Scenarios to Correlate: Failures ➡️ Success 
### Insight Gained  
- **Credential Stuffing/Brute-Force Attack Confirmation:** A pattern of thousands of failures originating from one city/IP range, immediately followed by a successful login from a different or the same region, suggests the bad actor either moved or finally guessed the credentials.
## Actionable Intelligence
- Force password reset for the compromised user; block the successful IP if it doesn't match a legitimate known location (e.g., a VPN).


---
## Query Used  
<img width="1613" height="274" alt="image" src="https://github.com/user-attachments/assets/718b6678-3c62-429a-a9fb-e8ebde60afa2" />


