# Azure Sentinel SIEM Deployment

## Project Overview
This project demonstrates how to deploy **Azure Sentinel** as a **Security Information and Event Management (SIEM)** solution to monitor and alert on successful sign-ins to an Azure Virtual Machine (VM). 

## Features
✅ **Azure Sentinel** setup for security monitoring  
✅ **Virtual Machine (VM) Logging** using Azure Monitor Agent  
✅ **Custom Log Rule** to track successful sign-ins  
✅ **Real-time Alerts** for SIEM monitoring  

## Steps to Deploy
### 1️⃣ **Azure Account Registration**
- Create an Azure account at [portal.azure.com](https://portal.azure.com)

### 2️⃣ **Create a Virtual Machine (VM)**
- Configure a Windows/Linux VM on Azure.
- Enable logging and monitoring.

### 3️⃣ **Set Up Azure Sentinel**
- Create a Sentinel workspace in Azure.
- Add **Microsoft Defender** & security logs to Sentinel.

### 4️⃣ **Connect VM to Sentinel**
- Use **Azure Monitor Agent (AMA)** to send logs to Sentinel.
- Ensure security event logs are being collected.

### 5️⃣ **Create a Log Rule for Sign-in Monitoring**
- Define a **KQL (Kusto Query Language) Rule** to alert on successful VM logins.
- Example KQL Query:
  ```kql
  SecurityEvent
  | where EventID == 4624
  | where AccountType == "User"
  ```

### 6️⃣ **Monitor SIEM Alerts**
- Navigate to **Microsoft Sentinel** → **Incidents**.
- View real-time alerts for successful VM logins.


## Technologies Used
- **Microsoft Azure** (Sentinel, Monitor, Virtual Machines)
- **Kusto Query Language (KQL)**
- **Azure Monitor Agent (AMA)**


## Future Enhancements
🔹 Add **automated alerts** via **Azure Logic Apps**  
🔹 Expand **log monitoring** to include failed login attempts  
🔹 Integrate **Microsoft Defender** for endpoint security  

## Author
Tanish Rathore | 
https://tanishrathore.github.io | 
https://www.linkedin.com/in/tanish-rathore
