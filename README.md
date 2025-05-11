## Project Title: Automating an Audit-Driven Identity and Access Management Framework in Active Directory with Enhanced Security and Compliance

## Disclaimer Notice:
The use of the name "SidodatTech" in this project is for illustrative and educational purposes only. SidodatTech is a fictional company created for this project. Any resemblance to real companies, organizations, or individuals, living or dead, is purely coincidental. The information provided is intended for educational and research purposes. SidodatTech and other names used in this project do not endorse, sponsor, or approve any content, methodologies, or recommendations presented herein. All opinions, conclusions, and recommendations expressed in this project are solely those of the author and do not represent the views or positions of any actual company or organization. By viewing or utilizing this project, the reader acknowledges and agrees to these terms and conditions.

##	Scenario Background: SidodatTech AD DS Implementation and Management
SidodatTech Enterprise Limited is a mid-sized financial services company operating in a regulated environment, with a strong focus on digital transformation, client data protection, and compliance with industry standards such as ISO/IEC 27001, PCI-DSS, SOX, and local financial regulatory requirements. The organization’s Active Directory (AD) infrastructure serves as the backbone for user authentication, system access, and identity management across both its on-premises and hybrid cloud environments.
During a recent external compliance audit conducted by third-party assessors, SidodatTech experienced a significant audit failure due to critical deficiencies in its Identity and Access Management (IAM) and Active Directory governance practices. These failures highlighted systemic vulnerabilities and exposed the organization to compliance violations, insider threats, and reputational damage.

Key findings from the audit include:

•	Insufficient access controls and lack of alignment between user roles and granted permissions, violating the principle of least privilege.

•	Presence of orphaned and inactive accounts associated with former employees, contractors, and service accounts posing a risk of unauthorized access.

•	Absence of centralized, role-based access control (RBAC) structures, resulting in ad-hoc access provisioning and excessive permissions.

•	Inadequate audit trails and logging mechanisms, preventing traceability of user activities and privilege escalations.

•	Lack of automated processes for user provisioning, de-provisioning, and role reassignment, leading to manual errors and delayed account updates.

•	Unsegmented administrative access, where multiple privileged users share global access without justification or segregation of duties (SoD) enforcement.

These deficiencies significantly increased SidodatTech’s exposure to regulatory fines, operational disruptions, and insider threats, with downstream effects on its digital services, client trust, and audit readiness. In response, executive leadership approved a strategic initiative to remediate these IAM weaknesses by implementing an automated, audit-driven IAM framework within Active Directory. The solution aims to improve governance, automate identity lifecycle processes, and strengthen compliance posture using an Agile delivery model—allowing for incremental improvement and continuous feedback.

This project will serve as a foundational step in aligning SidodatTech’s access control environment with industry best practices, enabling proactive monitoring, policy enforcement, and scalable integration with future IAM solutions, including identity federation and zero-trust architecture.

## Executive Summary 

SidodatTech Enterprise Limited, a mid-sized financial services organization, has launched a strategic initiative to address the findings of a recent compliance audit that revealed severe deficiencies in its Active Directory (AD)-based Identity and Access Management (IAM) framework. These deficiencies included the presence of orphaned user accounts belonging to former employees, excessive and unregulated privileges due to inconsistent role-based access control (RBAC), a lack of audit trails for changes made to user and group accounts, and insufficient monitoring of privileged user activities. These gaps not only exposed the company to regulatory non-compliance but also increased the risk of data breaches, insider threats, and operational inefficiencies. In response, this project aims to design and implement an automated, audit-driven IAM framework that strengthens security, enhances compliance, and aligns user access with organizational policy through RBAC standardization and lifecycle management.

The outcome of this project is expected to produce tangible, measurable improvements. By the end of the implementation, the organization will have eliminated 100% of orphaned accounts in Active Directory, reduced excessive user permissions by at least 95% through RBAC enforcement, achieved 100% traceability of privileged activities via centralized audit logging, and fully remediated audit findings. Additionally, automation of user provisioning and de-provisioning processes is projected to result in a 30% reduction in administrative workload and time spent on access-related tasks.

Risk management is a cornerstone of this initiative. The project employs a structured approach to identify, assess, and mitigate risks related to unauthorized access, policy violations, and audit failures. Regular access reviews, automation of identity processes, and continuous monitoring of privileged account usage are integrated to reduce the attack surface and maintain adherence to compliance frameworks. Risk is measured both pre- and post-implementation using a residual risk scoring model, ensuring that control improvements directly reduce exposure and align with the organization's security governance policies.

A Business Impact Analysis (BIA) conducted during the planning phase highlighted that unresolved IAM issues could lead to substantial regulatory fines, client data exposure, and operational downtime. The ability of employees and systems to operate securely and efficiently hinges on proper access control. Therefore, this project plays a critical role in reducing the likelihood and impact of these scenarios by establishing accountability, ensuring only authorized personnel have access to sensitive systems, and minimizing the risk of data compromise or misuse.

In terms of business continuity, the IAM framework supports critical operational resilience. By embedding access control measures into the broader business continuity and disaster recovery strategies, the company can ensure that, even during disruptions or emergency situations, access is appropriately maintained, restricted, or adjusted in real-time. This level of automation and control is essential to maintaining trust, service delivery, and compliance under adverse conditions.

The project follows an Agile methodology to enable flexibility, iterative development, and continuous stakeholder involvement. The implementation is divided into six two-week sprints, each dedicated to a distinct area of IAM, such as account cleanup, RBAC modeling, audit trail configuration, and automation integration. Agile ceremonies including daily stand-ups, sprint planning, and retrospectives, ensure that the team responds promptly to feedback and evolving compliance requirements. Each sprint culminates in a stakeholder demonstration to validate progress and maintain alignment with business goals. This iterative model allows for rapid adaptation to challenges, early delivery of high-priority features, and overall improved project success.

By automating access governance and embedding audit capabilities across the identity lifecycle, SidodatTech is not only closing compliance gaps but also laying the groundwork for a resilient, secure, and scalable IT environment.

## Project Background

In the rapidly evolving regulatory and threat landscape of the financial services sector, Identity and Access Management (IAM) is no longer a convenience—it's a compliance and security imperative. SidodatTech Enterprise Limited, a mid-sized financial institution offering digital lending and asset management services, recently underwent a routine compliance audit triggered by industry regulatory bodies. The audit uncovered significant deficiencies in the organization’s Identity and Access Management (IAM) practices, particularly within its on-premises Microsoft Active Directory (AD) environment, which serves as the backbone for authentication, authorization, and access control across enterprise systems.

As financial institutions handle sensitive customer data and are prime targets for threat actors, these findings elevated the risk posture of the organization, both from a regulatory and operational standpoint. Upon internal review and consultation with external security auditors, it became clear that manual, inconsistent, and siloed IAM processes were not only impeding operational efficiency but also increasing the risk of data breaches, insider threats, and non-compliance with frameworks such as ISO/IEC 27001, SOX, and GDPR. To address these challenges, SidodatTech initiated a project to design and implement a fully automated, audit-driven IAM framework that enhances security, ensures regulatory compliance, and aligns with industry best practices. The framework is intended to eliminate control gaps, enforce the principle of least privilege, provide full visibility into user account lifecycle events, and deliver automated audit logs to support governance, risk management, and compliance (GRC) operations.

This initiative will be executed using the Agile project methodology to ensure iterative progress, stakeholder collaboration, rapid deployment of features, and continuous improvement based on real-time feedback. The outcome will not only resolve current audit findings but also position SidodatTech as a security-forward enterprise capable of scaling IAM capabilities in response to emerging threats and compliance mandates.


## 1.0	Introduction

In the modern digital enterprise, Identity and Access Management (IAM) serves as the cornerstone of cybersecurity and compliance strategy. As organizations increasingly digitize operations and migrate to hybrid cloud infrastructures, the risk of unauthorized access, insider threats, data breaches, and compliance violations has surged. Identity is the new security perimeter, and without effective IAM practices, enterprises are left vulnerable to both internal and external threats.

SidodatTech Enterprise Limited, a mid-sized financial services company, recently faced increasing regulatory pressures to uphold strong security and compliance postures. Identity and Access Management (IAM) has become a critical component of cybersecurity governance. However, a recent compliance audit at SidodatTech uncovered significant deficiencies in their Active Directory (AD) configuration, highlighting the need for a more structured and automated IAM framework. Key concerns included the presence of orphaned accounts, unmonitored privileged access, inconsistent role-based access assignments, and a lack of comprehensive audit logging. Such gaps not only expose organizations to internal and external threats but also breach key regulatory standards like ISO/IEC 27001, SOX, and NIST SP 800-53, posing severe financial, reputational, and legal consequences. Recognizing the urgency and severity of these issues, SidodatTech has initiated a strategic project to automate an audit-driven IAM framework in AD. This initiative is designed not only to address current compliance gaps but also to establish a robust, scalable, and secure access control infrastructure aligned with industry global best practices.

The need for a robust IAM framework is reinforced by global cybersecurity trends, with IAM becoming the backbone of enterprise security, especially in hybrid work settings and cloud-integrated infrastructures. According to the Gartner IAM Market Guide (2024), 85% of security incidents involve misuse of credentials or poorly managed access rights, with 61% directly linked to ineffective IAM controls [1]. The 2024 Cost of a Data Breach Report by the Ponemon Institute and IBM indicates that organizations lacking automated IAM systems face an average $1.3 million higher breach cost compared to those with integrated access management solutions [2]. In addition, the Ponemon Institute and Saviynt’s 2023 State of IAM Maturity Report found that 74% of organizations experience delays in removing access for departed employees, and 62% lack centralized visibility into privileged accounts. Moreover, Cybersecurity Ventures projects global IAM spending to surpass $25 billion USD by 2026, highlighting the sector’s growing prioritization of access governance [3].

This project, “Automating an Audit-Driven Identity and Access Management Framework in Active Directory with Enhanced Security and Compliance using Agile Model,” initiated by SidodatTech, is designed to automate a scalable, audit-focused IAM framework within its Active Directory infrastructure to strengthen security and sustain compliance. The project will focus on automating account reviews, implementing a structured RBAC model, removing orphaned accounts, logging administrative activity, and integrating audit trails with centralized SIEM systems. Leveraging Agile methodology will guide the project’s execution, enabling rapid iteration, continuous feedback, cross-functional collaboration, and faster time-to-value. Through structured sprints and prioritized deliverables, SidodatTech aims to foster a culture of accountability, visibility, and access hygiene across its enterprise.

Ultimately, this initiative represents more than a corrective measure it is a strategic investment in SidodatTech’s long-term security maturity, operational integrity, and compliance readiness in a risk-sensitive and regulated industry.


## 2.0	Project Scope

This project encompasses the full lifecycle of planning, designing, implementing, and operationalizing an automated, audit-driven Identity and Access Management (IAM) framework within SidodatTech’s Active Directory (AD) environment. The scope includes all user accounts, groups, organizational units (OUs), and administrative roles across the organization’s on-premises and hybrid AD infrastructure.

The core focus is to enhance identity governance by implementing consistent Role-Based Access Control (RBAC), automating user provisioning and de-provisioning processes, and integrating audit mechanisms to monitor privileged access and account changes. All legacy and inactive accounts will be reviewed, validated, and either remediated or deactivated to align with compliance mandates and internal security policies. The scope also includes the design of automated workflows for access approvals, terminations, and role changes using PowerShell scripting and integration with existing HR and ITSM systems.

Additionally, the project covers the deployment of a centralized audit logging and monitoring solution to provide real-time visibility into access control events, and to enable forensic analysis during security audits or incidents. The IAM framework will be assessed and tested against compliance frameworks such as ISO/IEC 27001, NIST SP 800-53, CIS Controls, and applicable financial sector regulatory requirements.

Out of scope for this project are broader enterprise security functions not directly related to identity lifecycle management, such as multifactor authentication (MFA) rollout, cloud-native IAM systems beyond Azure AD integration, and group policy management (GPO) configurations. These may be considered for future initiatives based on the outcomes and maturity of this deployment.

The project will be delivered in iterative phases using Agile methodology, ensuring stakeholder feedback and incremental deployment of high-impact IAM capabilities, while minimizing disruption to business operations.

In-Scope:

•	Review and analysis of existing AD user and group configurations.

•	Implementation of scripts/tools for automated account management.

•	Standardization and enforcement of RBAC.

•	Deployment of auditing and alert mechanisms for AD changes.

•	Integration with Security Information and Event Management (SIEM) tools for real-time monitoring.

•	User training and documentation for the IAM framework.

Out-of-Scope:

•	Group Policy Object (GPO) configuration.

•	Integration with third-party IAM platforms.

•	Identity federation or single sign-on (SSO) implementation.


## 3.0	Project Objectives

he primary objective of this project is to design, develop, and implement a robust, automated, and audit-driven Identity and Access Management (IAM) framework within SidodatTech’s Active Directory (AD) environment, in alignment with industry standards such as ISO/IEC 27001, NIST SP 800-53, and CIS Controls. The initiative seeks to establish a governance model that ensures access to enterprise systems is provisioned, modified, and de-provisioned based on verified roles and responsibilities, while maintaining a comprehensive audit trail to meet regulatory, legal, and operational requirements.

The primary objectives of this project are:

•	To automate user lifecycle management in Active Directory, including provisioning, modification, and de-provisioning.

•	To establish and enforce standardized RBAC policies across departments.

•	To identify and remediate orphaned and inactive accounts.

•	To implement audit logging mechanisms for privileged account activities and group changes.

•	To ensure ongoing compliance with relevant regulations such as ISO 27001, SOX, and NIST.

•	To enhance visibility into access rights and activities for continuous monitoring and reporting.

The objective is also to provide a scalable foundation for future identity federation, single sign-on (SSO), and cloud-based IAM integrations by following an extensible, modular design. Ultimately, the project will ensure that SidodatTech’s access control processes are not only secure and compliant but also agile, efficient, and aligned with the organization’s long-term digital transformation and cybersecurity strategy.


## 4.0  Technologies and Tools:
•	A computer system with 16GB RAM

•	A virtual machine preferably Oracle Virtual Box

•	Windows Server 2010 pro (WorkstationMachine)


•	Windows 2022 Server for Active Directory (AD-DC)

•	Ubuntu Server (Linux version 24.02 Lts): For Splunk Server

•	SIEM - Splunk

•	Sysmon-Sysinternal

•	Splunk Universal Forwarder

•	PowerShell scripts


## 5.0	Project Methodology: Agile-Based Implementation of an Audit-Driven IAM Framework

The implementation of "Automating an Audit-Driven Identity and Access Management Framework in Active Directory" follows a robust, industry-grade Agile methodology designed to accommodate complexity, regulatory sensitivity, and cross-functional collaboration. Given the dynamic nature of identity governance and the criticality of real-time compliance enforcement, the Agile Scrum framework is selected to promote adaptability, iterative delivery, stakeholder alignment, and continuous risk management.

5.1	Agile Justification

Unlike traditional Waterfall approaches, Agile allows security, compliance, and IT teams to incrementally assess, develop, and deploy IAM components while constantly integrating stakeholder feedback. The iterative nature of Scrum enables early detection of misalignments, better handling of regulatory changes, and rapid response to identity-related risks across the enterprise.
The project will follow the Agile methodology, ensuring flexibility, iterative delivery, and active stakeholder engagement. 

The key characteristics of the Agile model applied in this project include:

•	Sprints: Each phase will be divided into 2-week sprints, focusing on specific IAM components such as auditing, RBAC, automation, and de-provisioning.

•	Scrum Meetings: Daily stand-ups and weekly reviews will ensure transparent communication and rapid issue resolution.

•	Backlog Management: Requirements will be managed in a dynamic product backlog, prioritized by risk, compliance urgency, and technical feasibility.

•	Incremental Delivery: Each sprint will result in a functional increment that is tested and documented, enabling progressive enhancement of the IAM framework.

5.2 Project Timeline – IAM Automation with Agile Delivery

5.3	Stakeholder Analysis


5.4	Key meetings with the sprint phase



5.5 Project Team Structure
The success of this IAM automation project depends on a cross-functional team with clearly defined roles, responsibilities, and collaboration channels. The team structure below ensures technical depth, compliance oversight, business alignment, and agile delivery throughout the project lifecycle.

| Role	| Team Member / Department	| Key Responsibilities | Expertise Area |
|-------|--------------|------|-----|
| Project Sponsor | Chief Information Officer (CIO) | Approves funding and resources; champions project at the executive level; resolves strategic roadblocks. | Executive Leadership, IT Governance |
| Project Manager (Scrum Master)   |  IT Program Delivery Lead |  Manages Agile sprints, team coordination, progress tracking, stakeholder reporting, and risk mitigation. | Project Management, Agile, SDLC  |
|    |    |   |   |
|    |    |   |    |
|    |    |    |   |



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

1.	Installation and Configuration of Machines: Install and configure Windows 10 Workstation, Ubuntu Server for Splunk, and Windows Server 2022 for AD within Oracle VirtualBox.

2.	Active Directory Configuration: Set up Active Directory, including domain controllers and group policy objects (GPOs), and define initial role-based access control (RBAC) policies and audit parameters.

3.	SIEM Integration and Monitoring Setup: Configure Splunk and Splunk Universal Forwarder to collect and aggregate logs from Active Directory and deploy Sysmon-Sysinternal for advanced event monitoring.

Expected output: A fully designed framework, including system architecture and configurations.



Phase 3 – Implementation:

This phase involves putting the designs into action to create the audit-driven IAM framework. Major activities at the implementation stage are:

•	Deploy and validate the configuration of all machines and software.

•	Implement automated workflows for user account lifecycle management (e.g., account creation, modification, and deactivation).

•	Enable real-time monitoring and alerting for unauthorized access and privilege escalation using Splunk and Sysmon.

•	Enforce RBAC and ensure users only have access relevant to their roles.

•	Implement audit trails for all AD activities, ensuring logs are comprehensive and tamper-proof.

•	Create User Accounts and Service Accounts  in their respective Organisational Units.

•	Create separate administrative groups with restricted permissions and establish a monitoring system for privileged accounts.

•	Review and revise Active Directory settings to enforce strong password policies, account lockouts, and a classification system based on the principle of least privilege.

•	Conduct a business function review to create specific roles, ensuring users only have access to the resources necessary for their job functions.

•	Configure ACLs in AD to ensure appropriate permissions are applied to different user groups based on their roles.

•	Develop a PowerShell script to identify orphaned accounts by comparing Active Directory data with HR records. The script will automatically disable or remove these accounts.

•	Implement regular checks for inactive or unnecessary accounts.

•	Configure Active Directory to log changes to user accounts, security groups, and group memberships. All administrative activities will be tracked and logged for accountability.

•	Use tools like Splunk or Microsoft Advanced Threat Analytics (ATA) to collect and analyze logs for unusual or suspicious activities.

•	Set up automated alerts for suspicious changes, such as unauthorized group memberships or changes in user permissions.

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



 ![ADx Windows10Fig6](https://github.com/user-attachments/assets/231b5665-674a-492c-af32-884148dbdb39)

Figure 5.1.1d:


![ADx Windows10Fig6](https://github.com/user-attachments/assets/40a9e117-de9b-4b45-9c43-b77a1111b4aa)

Figure 5.1.1e: Windows 10 media creation tool 





•	Windows 10 Installation in Virtual Box

![ADx Windows10Fig10](https://github.com/user-attachments/assets/7478cc9c-496f-4931-b62b-1c927d79f507)

Figure 5.1.1f:


![ADx Windows10Fig7](https://github.com/user-attachments/assets/00baf969-8f1a-4f8d-8567-cb1365d68fd5)

Figure 5.1.1g:


![ADx Windows10Fig9](https://github.com/user-attachments/assets/dbd43619-d0bf-46cb-a8a0-6d459082051a)

Figure 5.1.1h:

Creating Windows 10 Pro Virtual Machine on VirtualBox


![ADx Windows10Fig11](https://github.com/user-attachments/assets/e759e6ab-e128-42b8-bc93-1c7a61b1f6c5)

Figure 5.1.1i: Windows 10 Pro WorkStation Machine

![ADx Windows10Fig12](https://github.com/user-attachments/assets/bccd1797-cf02-4472-8b79-f022010c2e8d)

Figure 5.1.1j:
Accept the Licence Agreement


![ADx Windows10Fig16](https://github.com/user-attachments/assets/4d76e21f-8b7f-40a5-95d5-3dbb30c417ed)

Figure 5.1.1k:


![ADx Windows10Fig18](https://github.com/user-attachments/assets/ccd6796c-fa46-4173-b804-e7818c738a0c)

Figure 5.1.1l: Windows 10 Pro Setup



5.1.2	Windows Server 2022 Installation for Active Directory

•	Downloading the ISO file from https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022 

![AD WindowsServerFig1](https://github.com/user-attachments/assets/e96387db-7b8d-4318-9547-30b4f6e081de)

Figure 5.1.2a: Windows Server 2022


![AD WindowsServerFig2](https://github.com/user-attachments/assets/2a02c4cf-d8d6-426c-aef7-427d8d2a55aa)

Figure 5.1.2b: Windows Server 2022 iso


 ![AD WindowsServerFig5](https://github.com/user-attachments/assets/3e0daf08-2a08-4fa1-825d-7f4b2474e916)

Figure 5.1.2c: Windows Server 2022 in the Downloads


•	Add the Windows Server 2022 ISO file to the VirtualBox

![AD WindowsServerFig11](https://github.com/user-attachments/assets/90085aa2-cc47-44b3-9f57-ce4232f76d86)

Figure 5.1.2d:

![AD WindowsServerFig12](https://github.com/user-attachments/assets/257b23db-4ed4-46ae-a997-99f872d1edb4)

Figure 5.1.2e:


![AD WindowsServerFig13](https://github.com/user-attachments/assets/92b383c1-9bdf-4756-b0d4-6df9e4cca491)

Figure 5.1.2f:

![AD WindowsServerFig14](https://github.com/user-attachments/assets/90433b9e-30c8-4d78-897a-9d41e6a75a2e)
Figure 5.1.2g:

![AD WindowsServerFig15](https://github.com/user-attachments/assets/08c70839-aa3b-4dd5-8b11-c7ad3496f9ad)

Figure 5.1.2h: 

![AD WindowsServerFig16](https://github.com/user-attachments/assets/eb110b96-6a24-42f1-8c6f-ee0d7ce79a17)

Figure 5.1.2i:


![AD WindowsServerFig17](https://github.com/user-attachments/assets/de612023-95b0-4ae1-b744-91423a1b5af1)
Figure 5.1.2j:


•	Setting up the Windows Server 2022
Create Login Credentials

![AD WindowsServerFig18](https://github.com/user-attachments/assets/8b845654-a1c3-44f5-aceb-63bf76c5ee32)

Figure 5.1.2k: Create login details

•	Select Devices >> Keyboard >> Insert Ctrl-ALT-Del


![AD WindowsServerFig19](https://github.com/user-attachments/assets/9ef2ffd4-8ac3-4487-854f-f6c97c2e9f24)

Figure 5.1.2l:

Logon to the Active Directory Server
 
Figure 5.1.2m:

XXXXX
Figure 5.1.2n: Server Manager created.



5.1.3	Ubuntu Server (Linux version 24.02 LTS) for Splunk Server

•	Download Ubuntu Server from https://ubuntu.com/download/server#products

![Ubuntu-SplunkServerFig2](https://github.com/user-attachments/assets/36a1c6a1-bf28-4305-b878-d8a06e358409)
Figure 5.1.3a: Ubuntu server download


![Ubuntu-SplunkServerFig4](https://github.com/user-attachments/assets/9affe84f-63a9-4f18-8997-eadfd681c42d)
Figure 5.1.3b: Downloading Ubuntu server 


![Ubuntu-SplunkServerFig9](https://github.com/user-attachments/assets/5ab11641-c506-4b37-b841-7274be1ecc76)
Figure 5.1.3c: Ubuntu server iso in the Downloads

•	Ubuntu server installation on VirtualBox

![Ubuntu-SplunkServerFig10a](https://github.com/user-attachments/assets/569a8332-3ed8-4a6d-840b-6e6b1724f7e4)
Figure 5.1.3d: Splunk Server installation in VirtualBox


![Ubuntu-SplunkServerFig10](https://github.com/user-attachments/assets/0dcb285a-8014-48e5-ba5a-62ed6418aa95)
Figure 5.1.3e: Creating name and iso file uploading

•	Set the Base memory to 8GB and CPU to 2


![Ubuntu-SplunkServerFig11](https://github.com/user-attachments/assets/bf08f33f-4c28-4128-96ff-299ede9615d1)
Figure 5.1.3f: Hardware set-up



•	Set the Hard disk size to 100GB


![Ubuntu-SplunkServerFig12 jpg](https://github.com/user-attachments/assets/31eb9509-3964-42f0-9b02-abdcc66e90bf)
Figure 5.1.3g: Hard disk size configuration


![Ubuntu-SplunkServerFig13](https://github.com/user-attachments/assets/0001a962-8265-48a2-8ab6-635353c434f1)
Figure 5.1.3h: Spunk installation 


Splunk Configuration

•	Select English and press Enter. Continue to select Done

![Ubuntu-SplunkServerFig14](https://github.com/user-attachments/assets/74364fcf-2998-43c1-949b-ba672a2749d4)
Figure 5.1.3i: Splunk profile set-up


Login credential set-up

![Ubuntu-SplunkServerFig18](https://github.com/user-attachments/assets/f9a64d5b-3355-456a-ac7c-abd823e1e421)
Figure 5.1.3j: Splunk server installation login set-up


![Ubuntu-SplunkServerFig22](https://github.com/user-attachments/assets/d24d91bf-af60-4612-b3d3-413882e4fbee)
Figure 5.1.3k:


![Ubuntu-SplunkServerFig26](https://github.com/user-attachments/assets/f22b404c-5e13-4f81-8794-e0785b9be919)
Figure 5.1.3l: Spunk sign-in page


•	Splunk upgrade and update the server


![Ubuntu-SplunkServerFig26](https://github.com/user-attachments/assets/877aedf5-72c4-420a-9e8e-d14d61876045)
Figure 5.1.3m: Splunk upgrade




5.1.4	Configuring the NAT Network of the Virtual Box and Splunk Server

•	Configuring the NAT Network of the Virtual Box 

![SysmonFig3](https://github.com/user-attachments/assets/835648a3-07d8-4a22-a286-b40e017a8d85)

Figure 5.1.4a: Virtual Box NAT Network set-up

•	Configuring the NAT Network of the Splunk Server 

![SysmonFig4](https://github.com/user-attachments/assets/bfa4f66a-9079-43e8-9775-50e2ab467d0d)
Figure 5.1.4b: Splunk NAT Network set-up

XXXXXX
Figure 5.1.4c: Splunk NAT Network configuration


![SysmonFig20](https://github.com/user-attachments/assets/8a9b7e00-6129-4b7a-86fa-62496dd7df1f)
Figure 5.1.4d:


![SysmonFig22a](https://github.com/user-attachments/assets/6efc4831-1982-4796-8255-1773f1873385)
Figure 5.1.4e:


![SysmonFig24](https://github.com/user-attachments/assets/0c204216-53ed-4bb0-a523-d0a34fdfe943)
Figure 5.1.4f:


![SysmonFig25](https://github.com/user-attachments/assets/b7d0aca2-083b-4fde-91e7-23a096027534)
Figure 5.1.4g:


![SysmonFig26](https://github.com/user-attachments/assets/51b8adf5-4c5b-4f7d-8e03-d8a319bc28ee)
Figure 5.1.4h:

xxxxxx 
Figure 5.1.4i:


![SysmonFig30a](https://github.com/user-attachments/assets/32ccd3f7-2381-4146-b8e5-4ab687bea21f)

Figure 5.1.4j:


Click on Add
 
 
![SysmonFig31a](https://github.com/user-attachments/assets/feb1b88c-7bde-4207-a106-37fb2eb072ed)

Figure 5.1.4k:


![SysmonFig31](https://github.com/user-attachments/assets/38d5a430-a257-4b81-a1ac-600e9053a632)
Figure 5.1.4l:


![SysmonFig32](https://github.com/user-attachments/assets/a0cce85e-0178-44bc-9563-2064beea1fbb)
 
Figure 5.1.4m:


![SysmonFig33](https://github.com/user-attachments/assets/13bdd0c4-7178-431f-9a63-7136d8f21540)

Figure 5.1.4n:


![SysmonFig34](https://github.com/user-attachments/assets/fa5f2b21-27f8-490c-9f67-822f1785d1cd)

Figure 5.1.4o:


![SysmonFig35](https://github.com/user-attachments/assets/91fdaadb-6a08-4766-950d-8b6f8bf95aa8)

Figure 5.1.4p:


![SysmonFig36](https://github.com/user-attachments/assets/656937df-da4f-4e84-81e0-6052de7c5488)
Figure 5.1.4q:


![SysmonFig38](https://github.com/user-attachments/assets/ceb81509-c4b8-4f74-b2c8-ade287b38300)
Figure 5.1.4r:


![SysmonFig40a](https://github.com/user-attachments/assets/48bbf943-1bfa-4339-87e2-f71e85e02d6c)

Figure 5.1.4s:


5.1.5	Installation and Configuration of Sysmon and Splunk Universal Forwarder on WorkStationMachine and Splunk Server
Rename the target machine to WorkStationMachine:
 
Figure 5.1.4s:

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






