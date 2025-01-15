## Project Title: Automating an Audit-Driven Identity and Access Management Framework in Active Directory with Enhanced Security and Compliance

## Disclaimer Notice:
The use of the name "SidodatTech" in this project is for illustrative and educational purposes only. SidodatTech is a fictional company created for the purpose of this project. Any resemblance to real companies or organizations and individual, living or dead, is purely coincidental. The information provided is intended for educational and research purposes. SidodatTech and other names used in this project, does not endorse, sponsor, or approve of any of the content, methodologies, or recommendations presented herein. All opinions, conclusions, and recommendations expressed in this project are solely those of the author and do not represent the views or positions of any actual company or organization.
By viewing or utilizing this project, the reader acknowledges and agrees to these terms and conditions.

## Scenario Background:
SidodatTech Enterprise Limited, a mid-sized financial services company, experienced a compliance audit failure due to weak access control mechanisms, insufficient audit logs, and improper user and group management in their Active Directory (AD) environment. Regulators identified the following issues:
•	Lack of accountability for privileged user activities.
•	Orphaned accounts belonging to former employees still active in the system.
•	Inconsistent role-based access control (RBAC) policies, leading to excessive permissions for users.
•	Absence of audit trails for changes made to user accounts and security groups.
To address these challenges, SidodatTech aimed to design and implement an Identity and Access Management (IAM) framework that emphasizes auditing in Active Directory to ensure compliance, enhance security posture, and prevent unauthorized access.

This project aims to implement a systematic process for reviewing and monitoring user accounts in Active Directory (AD) to ensure proper Identity and Access Management (IAM). The focus will be on maintaining the principle of least privilege, identifying inactive or stale accounts, tracking permissions, and detecting suspicious activities. The goal is to safeguard the organization’s resources, improve compliance with security standards, and enhance access control.







## 1.0	Introduction
In the digital age, organizations are increasingly reliant on their IT infrastructure for conducting daily operations, and one of the most critical aspects of that infrastructure is effective Identity and Access Management (IAM). IAM systems are designed to control who has access to the company's resources and ensure that access is appropriate based on the user's role and responsibility within the organization. 
The global Identity and Access Management (IAM) market generated revenues estimated at nearly 16 billion U.S. dollars in 2022 and is projected to reach a value of US$17.31 billion by 2023. It is forecasted that the market value of IAM will increase to 43.1 billion U.S. dollars by 2029 (https://www.statista.com/statistics/1445717/global-identity-and-access-management-market-value/)

 

Source : https://www.fortunebusinessinsights.com/industry-reports/identity-and-access-management-market-100373

Importance of IAM
According to The Institute of Internal Auditors (The IIA) in Global Technology Audit Guide (GTAG), it is important to examine the many reasons why organizations embark on IAM projects. These include: 
•	Improved regulatory compliance. 
•	Reduced information security risk. 
•	Reduced IT operating and development costs. 
•	Improved operating efficiencies and transparency. 
•	Improved user satisfaction. 
•	Increased effectiveness of key business initiatives

For companies like SidodatTech, an IAM system that not only manages users and their permissions but also audits activities and ensures compliance with regulatory standards is crucial. SidodatTech, a mid-sized financial services company, experienced a significant setback when they failed a compliance audit due to weak access control mechanisms and insufficient monitoring in their Active Directory (AD) environment. 

https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/audit-policy-recommendations

Active Directory Auditing and Compliance
Active Directory (AD), a directory service developed by Microsoft, is a central component of IAM in many organizations due to its robust capabilities for managing users, groups, and permissions. Microsoft AD is a structured data repository for storing directory data objects. It can be used to manage your organization’s IT resources, such as network infrastructure, email services, public key infrastructure (PKI) services, and wireless services.  Active Directory (AD) is a critical component in many organizations, serving as the central system for managing user identities, permissions, and access to network resources. Its central role makes it a prime target for cyber attackers aiming to gain unauthorized access to sensitive information and systems.

Compromising AD can grant attackers extensive control over an organization's IT infrastructure. The primary reasons include centralized control, privilege escalation, data exfiltration, persistence and lateral movement and difficulty in detection. Monitoring and auditing Active Directory (AD) are essential for maintaining security and compliance within an organization. According to Microsoft's best practices for securing Active Directory, it's crucial to monitor AD for signs of attack or compromise. This involves using legacy audit categories and audit policy subcategories, or Advanced Audit Policy, to detect unauthorized access, privilege escalations, or group policy modifications promptly. 

Key Elements to Audit in Active Directory
•	Logon Events: Track successful and failed logon attempts to identify potential brute force attacks or unauthorized access. 
•	Privilege Escalation and Role Changes: Monitor changes to privileged groups or roles, such as additions to Domain Admins or Enterprise Admins, to prevent unauthorized access. 
•	User Account Management: Detect the creation, deletion, or modification of user accounts, especially those involving administrative privileges or sensitive roles. 
•	Group Policy Changes: Audit modifications to Group Policy Objects (GPOs), which can have a significant impact on network security and operations. Source: Microsoft Active Directory Security

Tools for Auditing Active Directory
Microsoft's Native Tools:
•	Event Viewer: Provides logs for security, system, and application events.
•	Advanced Audit Policy: Allows fine-grained auditing of AD activities.
Third-Party Solutions
•	Netwrix Auditor: Comprehensive auditing, reporting, and compliance tool for AD.
•	Lepide Auditor: Focused on monitoring, alerting, and auditing of AD changes.
•	Splunk: Provides real-time analysis of AD logs with anomaly detection capabilities. - Integrates AD logs into a centralized SIEM for advanced analytics. Real-time log correlation and threat detection. 
Customizable dashboards and reports. 

By systematically auditing and monitoring Active Directory, organizations can enhance their security posture, ensure compliance, and reduce the risk of unauthorized access or breaches.

## 2.0	Scope
The project aims to design and implement a robust audit-driven Identity and Access Management framework using Active Directory (AD) to enhance security, ensures regulatory compliance, and prevents unauthorized access through effective auditing, role management, monitoring and improve accountability within the organization’s IT environment.

3.0	Project Objectives
The goal of this project is to implement a robust audit-driven IAM framework, focusing on the following objectives:
1.	Install and configure Windows 10 Workstation, Ubuntu server for Splunk, Windows server 2022 for Active Directory Server and Kali Linux.
2.	To establish robust, audit-focused Identity and Access Management (IAM) policies within Active Directory to effectively govern privileges, access permissions, user accounts, service accounts, and group memberships, ensuring security and compliance alignment.
3.	Automate User Account Lifecycle Management of user account creation, modification, and deactivation process to effectively reduce the risks from orphaned or inactive accounts and stale permissions.
4.	Deploy real-time monitoring and anomaly detection mechanisms to identify unauthorized access, privilege escalations, or group policy modifications promptly, ensuring swift threat mitigation.
5.	Enforce role-based access control (RBAC) to ensure users only have access to resources necessary for their roles to minimize excessive permissions and enhance organizational security posture.
6.	Implement detailed logging and audit trail capabilities across all Active Directory activities to align with regulatory compliance frameworks while enhancing transparency and accountability.

## 3.0  Technologies and Tools:
•	A computer system with 16GB RAM
•	A virtual machine preferably Oracle virtual Box
•	Windows server 2010 pro (WorkstationMachine)
•	Windows 2022 Server for Active Directory (AD-DC)
•	Ubuntu Server (Linux version 24.02 Lts) : For Splunk Server
•	SIEM - Splunk
•	Sysmon-Sysinternal
•	Splunk Universal Forwarder
•	PowerShell scripts


## 4.0 Methodology:
Phase 1 – Planning:
This phase focuses on preparing for the project's implementation by addressing resource allocation, communication, stakeholder engagement, and timeline considerations. The activities include:
•	Identify and procure necessary hardware and software (e.g., systems with 8GB RAM, Oracle VirtualBox, Windows Server, Ubuntu Server, and Splunk).
•	Assess and select free or cost-effective editions of required tools, ensuring their compatibility and security.
•	Define communication channels and medium for the project 
•	Schedule stakeholder meetings for each phase of the project that align with project goals.
•	Document project disclaimers, legal considerations, tools, technologies, resources, designs, processes, changes, and expected outcomes.
•	Draft a comprehensive project timeline.
Expected output: A detailed project plan, including schedules, resources, and tools inventory.

Phase 2 – Project Design:
This phase involves designing the technical and logical architecture required to achieve the project's objectives. The project is divided into three main sub-stages:
1.	Installation and Configuration of Machines: Install and configure Windows 10 Workstation, Ubuntu Server for Splunk, Windows Server 2022 for AD on within Oracle VirtualBox.
2.	Active Directory Configuration: Set up Active Directory, including domain controllers and group policy objects (GPOs) and define initial role-based access control (RBAC) policies and audit parameters.
3.	SIEM Integration and Monitoring Setup: Configure Splunk and Splunk Universal Forwarder to collect and aggregate logs from Active Directory and deploy Sysmon-Sysinternal for advanced event monitoring.
Expected output: A fully designed framework, including system architecture and configurations.

Phase 3 – Implementation:
This phase involves putting the designs into action to create the audit-driven IAM framework. Major activities at implementation stage are:
•	Deploy and validate the configuration of all machines and software.
•	Implement automated workflows for user account lifecycle management (e.g., account creation, modification, and deactivation).
•	Enable real-time monitoring and alerting for unauthorized access and privilege escalation using Splunk and Sysmon.
•	Enforce RBAC and ensure users only have access relevant to their roles.
•	Implement audit trails for all AD activities, ensuring logs are comprehensive and tamper-proof.
Expected output: A fully functional IAM framework in the Active Directory environment.



Phase 4 – Evaluation:
This phase focuses on testing the framework to ensure it meets security, compliance, and operational requirements. The following activities will be performed: 
•	Simulate unauthorized access attempts to test anomaly detection capabilities.
•	Perform access reviews to validate RBAC policies.
•	Generate compliance reports to ensure alignment with standards like SOX and ISO 27001.
•	Gather stakeholder feedback on framework usability and performance.
Expected output: Evaluation report highlighting findings, adjustments, and framework effectiveness.

Phase 5 – Documentation and Handover:
This phase ensures that stakeholders have the necessary resources to manage and maintain the framework. The final stage of the project will involve: 
•	Develop detailed user manuals, including processes for monitoring, auditing, and RBAC management.
•	Provide training to IT teams and administrators on framework operation.
•	Document lessons learned, project challenges, and future recommendations.
•	Officially hand over the system to the organization's IT team.
Expected output: Comprehensive documentation, trained personnel, and a fully operational IAM system in AD.


## 5.0 Result
5.1	Installation and configuration of machines
A total of four machines will be installed and configured on an Oracle Virtual Box. These machines are:
1.	Windows 10 Pro as WorkStationMachine
2.	Windows 2022 Server for Active Directory
3.	Ubuntu Server for Splunk server
4.	Other installations will include Splunk Universal Forwarder, Windows Event Viewer, and Sysmon-Sysinternal

5.1.1	Windows 10 Pro Installation for WorkStation Machine
•	Download Windows ISO image file from https://www.microsoft.com/en-ca/software-download/windows10

![ADx Windows10Fig1](https://github.com/user-attachments/assets/984b9ce6-5c3e-4f32-8a9f-444557de955a)

Figure 5.1.1a:

![ADx Windows10Fig2](https://github.com/user-attachments/assets/bdec870d-c537-408c-8b68-7fb9cb0506ac)
Figure 5.1.1b:


![ADx Windows10Fig3](https://github.com/user-attachments/assets/7c12ebaf-a233-428a-96c6-bfd6d3557103)
Figure 5.1.1c:

 
Figure 5.1.1d:


 
Figure 5.1.1d: Windows 10 media creation tool 





•	Windows 10 Installation in Virtual Box
 
Figure 5.1.1e:

 
Figure 5.1.1f:

 
Figure 5.1.1g:

Creating Windows 10 Pro Virtual Machine on VirtualBox
 
Figure 5.1.1h: Windows 10 Pro WorkStation Machine
 
Figure 5.1.1i:


 
Figure 5.1.1j:

 
Figure 5.1.1k: Windows 10 Pro Setup

5.1.2	Windows Server 2022 Installation for Active Directory
Downloading the ISO file from https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022
 
Figure 5.1.2a: Windows Server 2022


 
Figure 5.1.2b: Windows Server 2022 iso


 
Figure 5.1.2c: Windows Server 2022 in the Downloads













•	Add the Windows Server 2022 ISO file to the VirtualBox
 
Figure 5.1.2d:

 
Figure 5.1.2e:

 
Figure 5.1.2f:

 
Figure 5.1.2g:
 
Figure 5.1.2h: 

 
Figure 5.1.2i:


 
Figure 5.1.2j:

•	Setting-up the Windows server 2022
Create Logon credentials
 
Figure 5.1.2k : Create login details

•	Select Devices >> Keyboard >> Insert Ctrl-ALT-Del
 
Figure 5.1.2l:

Logn to the Active Directory Server
 
Figure 5.1.2m:

XXXXX
Figure 5.1.2n: Server Manager created


5.1.3	Ubuntu Server (Linux version 24.02 LTS) for Splunk Server
Download Ubuntu Server from https://ubuntu.com/download/server#products

 
Figure 5.1.3a: Ubuntu server download

 
Figure 5.1.3b: Downloading Ubuntu server 

 
Figure 5.1.3c: Ubuntu server iso in the Downloads

•	Ubuntu server installation on VirtualBox
 
Figure 5.1.3d: Splunk Server installation in VirtualBox








 
Figure 5.1.3e: Creating name and iso file uploading

•	Set the to Base memory to 8GB and CPU to 2
 
Figure 5.1.3f: Hardware set-up



•	Set the Hard disk size to 100GB
 
Figure 5.1.3g: Hard disk size configuration

Splunk Configuration
 
Figure 5.1.3h: Spunk installation 

Splunk Configuration
•	Select English and press Enter. Continue to select Done
 
Figure 5.1.3i: Splunk profile set-up

Login credential set-up
 
Figure 5.1.3j: Splunk server installation login set-up

 
Figure 5.1.3k: Hard disk size set-up

 
Figure 5.1.3l: Spunk sign-in page


Splunk upgrade and update the server
 
Figure 5.1.3m: Splunk upgrade

5.1.4	Configuring the NAT Network of the Virtual Box and Splunk Server
Configuring the NAT Network of the Virtual Box
 
Figure 5.1.4a: Virtual Box NAT Network set-up
Configuring the NAT Network of the Virtual Box
 
Figure 5.1.4b: Splunk NAT Network set-up

 
Figure 5.1.4c: Splunk NAT Network configuration


 
Figure 5.1.4d:

  
 
Figure 5.1.4e:


 
Figure 5.1.4f:

 
Figure 5.1.4g:
 
Figure 5.1.4h:

 
Figure 5.1.4i:
 
Figure 5.1.4j:


Click on Add
 
Figure 5.1.4k:

 
Figure 5.1.4l:

 
				Figure 5.1.4m:

 
Figure 5.1.4n:
 
Figure 5.1.4o:

 
Figure 5.1.4p:
 
Figure 5.1.4q:

 
Figure 5.1.4r:
 
			Figure 5.1.4s:
5.1.5	Installation and Configuration of Sysmon and Splunk Universal Forwarder on WorkStationMachine and Splunk Server
Rename the target machine to WorkStationMachine:
 

Change the IP address 192.168.10.7 on the network adapter to 192.168.10.100 
xxxxxxx
 

To access the Splunk server from the WorkStationMachine, browse 192.168.10.10:8000 on the WorkStationMachine web browser. 
 


Installation of Splunk Universal Forwarder
Logon to the Splunk account:
 


 


 

 

 

 



 


 





Installation of Sysmon on the WorkStationMachine
Download Sysmon v15.15 from https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon
 

Download Sysmon by Olaf config from https://github.com/olafhartong/sysmon-modular
 

 


 

 

Extract Symon file 
 

Copy the Sysmon folder path
 


 
Paste the Sysmon path to change to the Sysmon folder:
Type Sys and press Tab to display .\Sysmon64.exe -i(to specify configuration file) ..(to go back to a directory 2 step back), \Sysmon and press Tab to display sysmonconfig.xml 
 


 

 


To set instruction on Splunk Universal Forwarder on Event to send to Splunk Server by configuring input.conf in the local directory.

 
 

Save the Splunk Universal Forwarder Event instuctions in Notepad and save as input.conf
 



Save the Notepad in C:\\Program Files\SplunkUniversalForwarder\etc\system\local. Save as type – All Files
Note: Anytime the input.cof file is edited, Slunk Universal Forwarder must be restart. 
 

To restart Splunk Universal Forwarder in Services:
 

Double click the Splunk Universal Forwarder and select Log on tab
 

Select Local System account. Click Apply and Ok for the prompt.
 


 

 

Start the Splunk Universal Forwarder service:
 

Logon to Splunk server:
 


Select Settings
 


 
To create Endpoint Indexes, Select New Index, print the Index name and select Endpoint for Index Data Type
 


 



To enable Splunk server to receive data. Click Settings >> Forwarding and Receiving
 


 


 


 

 

 

5.1.4






