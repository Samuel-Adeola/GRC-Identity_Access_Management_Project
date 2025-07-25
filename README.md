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

##	Table of Contents

Executive Summary

Project Background

1. Introduction

2. Problem Statement

3. Objectives

4. Scope

5. Technical Tools and Technologies

6. Project Methodology - Agile Model: Justification, Project Team and Stakeholders, Roles and Responsibilities, Project Timeline, Stakeholders and Meetings, Roles and Responsibilities, Communication Plan

7. Risk Management

8. Implementation Stages

9. Testing and Validation

10. Expected Outcomes and Success Criteria

11. Conclusion

12. References

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

•	A virtual machine, preferably Oracle VirtualBox

•	Windows Server 2010 Pro (WorkstationMachine)

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

| Stakeholder | Role/Title | Interest in Project | Influence Level| Engagement Strategy |
|----|----|----|----|----|
| Chief Information Security Officer (CISO) | Executive Sponsor | Ensure IAM aligns with regulatory, risk, and security requirements. | High | Regular briefings, executive dashboards, risk updates. |
| IT Security Manager | Project Champion / Functional Owner | Accountable for enforcing security controls and IAM governance. | High | Actively involved in requirements gathering, sprint reviews, and risk assessment. |
| IAM Administrator | Technical Lead / SME | Responsible for implementing AD changes, scripting automation, and role assignments. | Medium | Involved in technical design, UAT, and deployment phases. |
| Infrastructure Team | AD / Network Admins | Manage the AD servers and related systems impacted by the changes.| Medium | Consulted on implementation, automation, and rollback procedures. |
| Compliance and Risk Team | Internal Auditors / Governance Specialists | Ensure framework meets regulatory and audit requirements. | High | Frequent check-ins, audit log validation, compliance testing. |
| Human Resources (HR) | Identity Source System Owner | Provides joiner/mover/leaver data to trigger account provisioning workflows. | Medium | Collaborate during requirements gathering and data integration stages. |
| IT Service Desk |Frontline IAM Support | First-level support for access requests and issues. | Low | Training and knowledge transfer on new workflows. |
| Application Owners | Business System Custodians | Approve access requests and validate access based on roles. | Medium | Engage for RBAC definition and testing scenarios. |
| Legal and Regulatory Affairs | Risk Governance Compliance | Ensure privacy and data access compliance. | Medium | Provide legal input for audit and access governance policies. | 
| Project Manager (Agile Scrum Master) | Project Coordination | Coordinates Agile activities, backlog grooming, sprint planning, and reporting. | High | Full-time project engagement, stakeholder updates, and delivery tracking. |
| End Users | Employees / Contractors | Subject to new access control policies and provisioning workflows. | Low | Awareness training, user acceptance testing, and feedback loop. |
| External Auditors / Regulators | Compliance Oversight | Review access governance and AD controls in post-implementation audits. | High | Provide evidence, documentation, and compliance mapping. |



5.4	Key meetings with the sprint phase
5.4	Key meetings with the sprint phase

| Sprint Phase | Suggested Timeline | Meeting Frequency | Participants | Key Meetings Conducted | Purpose | 
|----|----|----|----|---|---|
| Sprint 0: Initiation & Planning | Week 1 – Week 2 | One-time / Weekly | Project Sponsor, Project Manager, Scrum Master, Business Analyst, Security Lead | Project Kickoff Stakeholder Onboarding Agile Tooling Setup | Align on goals, roles, governance; define success criteria, onboard stakeholders, set Agile tool/workspace (e.g., Jira, Confluence) | 
| Sprint 1: Requirements Gathering | Week 3 – Week 4 | Daily / Bi-weekly | Business Analyst, IAM Lead, Security Architect, Compliance Analyst, HRIS Analyst | Sprint Planning Requirements Workshops Daily Standups | Capture detailed IAM and compliance requirements; review audit gaps and access control needs; align stakeholder expectations | 
| Sprint 2: Design & Architecture | Week 5 – Week 6 | Daily / Weekly | IAM Lead, AD Engineer, DevOps, Security Architect, CAB Representative | Architecture Review Sprint Planning CAB Pre-Approval | Finalize AD object design, RBAC policies, and audit logging; obtain CAB input on proposed changes; break epics into implementable stories | 
| Sprint 3: Implementation & Integration | Week 7 – Week 8 | Daily / Bi-weekly | AD Engineer, DevOps, IAM Lead, QA Tester, Security Analyst | Daily Standups Integration Sync CAB Change Approval | Deploy automation scripts, connectors, and permission structures; test integrations with HRIS, SIEM; receive approval for deployment actions | 
| Sprint 4: Testing & Validation | Week 9 – Week 10 | Daily / Weekly | QA Tester, IAM Lead, Business Analyst, Compliance Officer | Sprint Review QA & UAT Planning Compliance Sync | Conduct validation testing, RBAC audits, and UAT scenarios; document issues; align with auditors and business stakeholders |
| Sprint 5: Deployment & Go-Live | Week 11 – Week 12 | Daily / Weekly | CAB, Security Lead, IAM Lead, PM, Service Desk Lead | Go-Live Readiness Review Final CAB Meeting Executive Review | Final checks before production deployment; ensure rollback plan, change approvals, business continuity plans, and stakeholder sign-off | 
| Sprint 6: Optimization & Closure | Week 13 – Week 14 | Weekly | Entire Project Team, Executives, Stakeholders | Lessons Learned Workshop Process Optimization Review Final Demo | Conduct post-implementation analysis; define next-phase roadmap; present executive-level outcome metrics and finalize documentation | 





5.5 Project Team Structure

The success of this IAM automation project depends on a cross-functional team with clearly defined roles, responsibilities, and collaboration channels. The team structure below ensures technical depth, compliance oversight, business alignment, and agile delivery throughout the project lifecycle.

| Role	| Team Member / Department	| Key Responsibilities | Expertise Area |
|-------|--------------|------|-----|
| Project Sponsor | Chief Information Officer (CIO) | Approves funding and resources; champions project at the executive level; resolves strategic roadblocks. | Executive Leadership, IT Governance |
| Project Manager (Scrum Master) |  IT Program Delivery Lead |  Manages Agile sprints, team coordination, progress tracking, stakeholder reporting, and risk mitigation. | Project Management, Agile, SDLC |
| IAM Lead Architect |  Senior Security Architect  |  Designs IAM strategy, defines RBAC, reviews architecture, ensures compliance alignment. | Identity & Access Management, Security Design |
| Active Directory Engineer | AD Domain Administrator | Executes AD cleanup, manages OUs, roles, permissions, and automates provisioning tasks. | Active Directory, Scripting, Windows Server |
| DevOps Automation Engineer | Infrastructure Automation Specialist | Develops provisioning/de-provisioning scripts using PowerShell/Ansible; integrates with CI/CD pipelines. | Automation, Infrastructure as Code (IaC) |
| Security & Compliance Analyst |  | Leads compliance analysis, performs internal audits, aligns implementation with ISO 27001, NIST, etc. | Compliance, Audit, Risk Management |
| Business Analyst (BA) | Business Process Consultant | Gathers IAM and access requirements, maps business roles to technical permissions, supports documentation. | Business Analysis, RBAC Mapping | 
| HR Systems Analyst | HRIS Specialist | Supplies employee data, defines joiner/mover/leaver process integration with AD. | HR Systems, Data Integration |
| SIEM Integration Specialist | Security Monitoring Engineer | Integrates AD logs with SIEM tools (e.g., Splunk), configures alerts and reporting. | Security Monitoring, SIEM |
| Quality Assurance (QA) Tester | IT Security Tester | Tests IAM features, validates RBAC logic, access controls, and audit functionality. | QA Testing, Security Validation |
| Change Advisory Board (CAB) Liaison | Change Manager | Coordinates deployment approvals, manages change impact assessments, and logs change requests. | ITIL, Change Management |

5.6		Communication Plan

A well-structured communication plan ensures transparency, fosters collaboration, and aligns stakeholder expectations throughout the project lifecycle. This plan is tailored for an Agile delivery model, incorporating both structured and adaptive communication elements.

5.6.1. Communication Objectives

•	Ensure timely dissemination of relevant information to all stakeholders.

•	Support Agile collaboration through continuous feedback and sprint-based updates.

•	Align technical, business, and compliance teams on deliverables and expectations.

•	Facilitate risk mitigation, issue resolution, and informed decision-making.

•	Promote user adoption and readiness through awareness and training.


5.6.2. Communication Matrix

| Communication Type | Audience | Purpose | Frequency |  | Owner |
|----|----|----|----|---|---|
| Project Kickoff Meeting | All Stakeholders | Introduce project, goals, roles, timelines | Once (Project Start) | MS Teams / Zoom | Project Manager |
| Daily Scrum Stand-up | Project Team (Technical & Functional) | Track progress, blockers, and coordinate work | Daily (15 mins) | MS Teams / Agile Board / Jira | Scrum Master |
| Sprint Planning Meeting | Project Team & Key Stakeholders | Define sprint goals, prioritize backlog | Biweekly | Jira / Confluence / MS Teams | Scrum Master / Product Owner |
| Sprint Review & Demo | All Stakeholders | Showcase deliverables and collect feedback | End of each Sprint | Zoom / PowerPoint / Live Demo | Scrum Master / Dev Team Lead |
| Compliance Sync Meetings | Risk, Audit, Security, Legal Teams | Align framework with regulatory expectations | Biweekly or Monthly | Zoom / Meeting Minutes | IT Security Manager |
| Technical Design Sessions | Security, IAM, Infrastructure Teams | Discuss architecture, automation, and RBAC models | As Needed (Sprint 1-3) | Whiteboard / Teams / Diagrams.net | IAM Lead / Technical Architect |
| Risk & Issue Reports | Project Sponsor, Compliance, PMO | Escalate risks/issues and propose mitigation plans | Weekly | Email / Risk Register Document | Project Manager |
| User Awareness Workshops | End Users, HR, Service Desk | Educate on access policy changes and IAM workflows | Sprint 4 & 5 | Webinars / Internal LMS / Email | IT Security Trainer |
| Project Status Reports | CISO, Executive Sponsors | High-level updates, progress, metrics | Biweekly | PowerPoint / Dashboard / Executive Summary | Project Manager |
| Post-Implementation Review | All Stakeholders | Evaluate success metrics and gather lessons learned | Project Closeout | Presentation / Report / Meeting | Project Manager / CISO |





## 6.0 Result
6.1	Installation and configuration of machines
A total of four machines will be installed and configured on an Oracle Virtual Box. These machines are:

1.	Windows 10 Pro as WorkStationMachine

2.	Windows 2022 Server for Active Directory

3.	Ubuntu Server for Splunk server


4.	Other installations will include Splunk Universal Forwarder, Windows Event Viewer, and Sysmon-Sysinternal



6.1.1	Windows 10 Pro Installation for WorkStation Machine

•	Download Windows ISO image file from https://www.microsoft.com/en-ca/software-download/windows10


![ADx Windows10Fig1](https://github.com/user-attachments/assets/984b9ce6-5c3e-4f32-8a9f-444557de955a)

Figure 6.1.1a:


![ADx Windows10Fig2](https://github.com/user-attachments/assets/bdec870d-c537-408c-8b68-7fb9cb0506ac)
Figure 6.1.1b:



![ADx Windows10Fig3](https://github.com/user-attachments/assets/7c12ebaf-a233-428a-96c6-bfd6d3557103)
Figure 6.1.1c:



 ![ADx Windows10Fig6](https://github.com/user-attachments/assets/231b5665-674a-492c-af32-884148dbdb39)

Figure 6.1.1d:


![ADx Windows10Fig6](https://github.com/user-attachments/assets/40a9e117-de9b-4b45-9c43-b77a1111b4aa)

Figure 6.1.1e: Windows 10 media creation tool 





•	Windows 10 Installation in Virtual Box

![ADx Windows10Fig10](https://github.com/user-attachments/assets/7478cc9c-496f-4931-b62b-1c927d79f507)

Figure 6.1.1f:


![ADx Windows10Fig7](https://github.com/user-attachments/assets/00baf969-8f1a-4f8d-8567-cb1365d68fd5)

Figure 6.1.1g:


![ADx Windows10Fig9](https://github.com/user-attachments/assets/dbd43619-d0bf-46cb-a8a0-6d459082051a)

Figure 6.1.1h:

Creating Windows 10 Pro Virtual Machine on VirtualBox


![ADx Windows10Fig11](https://github.com/user-attachments/assets/e759e6ab-e128-42b8-bc93-1c7a61b1f6c5)

Figure 6.1.1i: Windows 10 Pro WorkStation Machine

![ADx Windows10Fig12](https://github.com/user-attachments/assets/bccd1797-cf02-4472-8b79-f022010c2e8d)

Figure 6.1.1j:
Accept the Licence Agreement


![ADx Windows10Fig16](https://github.com/user-attachments/assets/4d76e21f-8b7f-40a5-95d5-3dbb30c417ed)

Figure 6.1.1k:


![ADx Windows10Fig18](https://github.com/user-attachments/assets/ccd6796c-fa46-4173-b804-e7818c738a0c)

Figure 6.1.1l: Windows 10 Pro Setup



6.1.2	Windows Server 2022 Installation for Active Directory

•	Downloading the ISO file from https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022 

![AD WindowsServerFig1](https://github.com/user-attachments/assets/e96387db-7b8d-4318-9547-30b4f6e081de)

Figure 6.1.2a: Windows Server 2022


![AD WindowsServerFig2](https://github.com/user-attachments/assets/2a02c4cf-d8d6-426c-aef7-427d8d2a55aa)

Figure 6.1.2b: Windows Server 2022 iso


 ![AD WindowsServerFig5](https://github.com/user-attachments/assets/3e0daf08-2a08-4fa1-825d-7f4b2474e916)

Figure 6.1.2c: Windows Server 2022 in the Downloads


•	Add the Windows Server 2022 ISO file to the VirtualBox

![AD WindowsServerFig11](https://github.com/user-attachments/assets/90085aa2-cc47-44b3-9f57-ce4232f76d86)

Figure 6.1.2d:

![AD WindowsServerFig12](https://github.com/user-attachments/assets/257b23db-4ed4-46ae-a997-99f872d1edb4)

Figure 6.1.2e:


![AD WindowsServerFig13](https://github.com/user-attachments/assets/92b383c1-9bdf-4756-b0d4-6df9e4cca491)

Figure 6.1.2f:

![AD WindowsServerFig14](https://github.com/user-attachments/assets/90433b9e-30c8-4d78-897a-9d41e6a75a2e)
Figure 6.1.2g:

![AD WindowsServerFig15](https://github.com/user-attachments/assets/08c70839-aa3b-4dd5-8b11-c7ad3496f9ad)

Figure 6.1.2h: 

![AD WindowsServerFig16](https://github.com/user-attachments/assets/eb110b96-6a24-42f1-8c6f-ee0d7ce79a17)

Figure 6.1.2i:


![AD WindowsServerFig17](https://github.com/user-attachments/assets/de612023-95b0-4ae1-b744-91423a1b5af1)
Figure 6.1.2j:


•	Setting up the Windows Server 2022
Create Login Credentials

![AD WindowsServerFig18](https://github.com/user-attachments/assets/8b845654-a1c3-44f5-aceb-63bf76c5ee32)

Figure 6.1.2k: Create login details

•	Select Devices >> Keyboard >> Insert Ctrl-ALT-Del


![AD WindowsServerFig19](https://github.com/user-attachments/assets/9ef2ffd4-8ac3-4487-854f-f6c97c2e9f24)

Figure 6.1.2l:

Logon to the Active Directory Server
 
Figure 6.1.2m:

XXXXX
Figure 6.1.2n: Server Manager created.



6.1.3	Ubuntu Server (Linux version 24.02 LTS) for Splunk Server

•	Download Ubuntu Server from https://ubuntu.com/download/server#products

![Ubuntu-SplunkServerFig2](https://github.com/user-attachments/assets/36a1c6a1-bf28-4305-b878-d8a06e358409)
Figure 6.1.3a: Ubuntu server download


![Ubuntu-SplunkServerFig4](https://github.com/user-attachments/assets/9affe84f-63a9-4f18-8997-eadfd681c42d)
Figure 6.1.3b: Downloading Ubuntu server 


![Ubuntu-SplunkServerFig9](https://github.com/user-attachments/assets/5ab11641-c506-4b37-b841-7274be1ecc76)
Figure 6.1.3c: Ubuntu server iso in the Downloads

•	Ubuntu server installation on VirtualBox

![Ubuntu-SplunkServerFig10a](https://github.com/user-attachments/assets/569a8332-3ed8-4a6d-840b-6e6b1724f7e4)
Figure 6.1.3d: Splunk Server installation in VirtualBox


![Ubuntu-SplunkServerFig10](https://github.com/user-attachments/assets/0dcb285a-8014-48e5-ba5a-62ed6418aa95)
Figure 6.1.3e: Creating name and iso file uploading

•	Set the Base memory to 8GB and CPU to 2


![Ubuntu-SplunkServerFig11](https://github.com/user-attachments/assets/bf08f33f-4c28-4128-96ff-299ede9615d1)
Figure 6.1.3f: Hardware set-up



•	Set the Hard disk size to 100GB


![Ubuntu-SplunkServerFig12 jpg](https://github.com/user-attachments/assets/31eb9509-3964-42f0-9b02-abdcc66e90bf)
Figure 6.1.3g: Hard disk size configuration


![Ubuntu-SplunkServerFig13](https://github.com/user-attachments/assets/0001a962-8265-48a2-8ab6-635353c434f1)
Figure 6.1.3h: Spunk installation 


Splunk Configuration

•	Select English and press Enter. Continue to select Done

![Ubuntu-SplunkServerFig14](https://github.com/user-attachments/assets/74364fcf-2998-43c1-949b-ba672a2749d4)
Figure 6.1.3i: Splunk profile set-up


Login credential set-up

![Ubuntu-SplunkServerFig18](https://github.com/user-attachments/assets/f9a64d5b-3355-456a-ac7c-abd823e1e421)
Figure 6.1.3j: Splunk server installation login set-up


![Ubuntu-SplunkServerFig22](https://github.com/user-attachments/assets/d24d91bf-af60-4612-b3d3-413882e4fbee)
Figure 6.1.3k:


![Ubuntu-SplunkServerFig26](https://github.com/user-attachments/assets/f22b404c-5e13-4f81-8794-e0785b9be919)
Figure 6.1.3l: Spunk sign-in page


•	Splunk upgrade and update the server


![Ubuntu-SplunkServerFig26](https://github.com/user-attachments/assets/877aedf5-72c4-420a-9e8e-d14d61876045)
Figure 6.1.3m: Splunk upgrade




5.1.4	Configuring the NAT Network of the Virtual Box and Splunk Server

•	Configuring the NAT Network of the Virtual Box 

![SysmonFig3](https://github.com/user-attachments/assets/835648a3-07d8-4a22-a286-b40e017a8d85)

Figure 6.1.4a: Virtual Box NAT Network set-up

•	Configuring the NAT Network of the Splunk Server 

![SysmonFig4](https://github.com/user-attachments/assets/bfa4f66a-9079-43e8-9775-50e2ab467d0d)
Figure 6.1.4b: Splunk NAT Network set-up

XXXXXX
Figure 6.1.4c: Splunk NAT Network configuration


![SysmonFig20](https://github.com/user-attachments/assets/8a9b7e00-6129-4b7a-86fa-62496dd7df1f)
Figure 6.1.4d:


![SysmonFig22a](https://github.com/user-attachments/assets/6efc4831-1982-4796-8255-1773f1873385)
Figure 6.1.4e:


![SysmonFig24](https://github.com/user-attachments/assets/0c204216-53ed-4bb0-a523-d0a34fdfe943)
Figure 6.1.4f:


![SysmonFig25](https://github.com/user-attachments/assets/b7d0aca2-083b-4fde-91e7-23a096027534)
Figure 6.1.4g:


![SysmonFig26](https://github.com/user-attachments/assets/51b8adf5-4c5b-4f7d-8e03-d8a319bc28ee)
Figure 6.1.4h:

xxxxxx 
Figure 6.1.4i:


![SysmonFig30a](https://github.com/user-attachments/assets/32ccd3f7-2381-4146-b8e5-4ab687bea21f)

Figure 6.1.4j:


Click on Add
 
 
![SysmonFig31a](https://github.com/user-attachments/assets/feb1b88c-7bde-4207-a106-37fb2eb072ed)

Figure 6.1.4k:


![SysmonFig31](https://github.com/user-attachments/assets/38d5a430-a257-4b81-a1ac-600e9053a632)
Figure 6.1.4l:


![SysmonFig32](https://github.com/user-attachments/assets/a0cce85e-0178-44bc-9563-2064beea1fbb)
 
Figure 6.1.4m:


![SysmonFig33](https://github.com/user-attachments/assets/13bdd0c4-7178-431f-9a63-7136d8f21540)

Figure 6.1.4n:


![SysmonFig34](https://github.com/user-attachments/assets/fa5f2b21-27f8-490c-9f67-822f1785d1cd)

Figure 6.1.4o:


![SysmonFig35](https://github.com/user-attachments/assets/91fdaadb-6a08-4766-950d-8b6f8bf95aa8)

Figure 6.1.4p:


![SysmonFig36](https://github.com/user-attachments/assets/656937df-da4f-4e84-81e0-6052de7c5488)
Figure 6.1.4q:


![SysmonFig38](https://github.com/user-attachments/assets/ceb81509-c4b8-4f74-b2c8-ade287b38300)
Figure 6.1.4r:


![SysmonFig40a](https://github.com/user-attachments/assets/48bbf943-1bfa-4339-87e2-f71e85e02d6c)

Figure 6.1.4s:


5.1.5	Installation and Configuration of Sysmon and Splunk Universal Forwarder on WorkStationMachine and Splunk Server
Rename the target machine to WorkStationMachine:
 
Figure 6.1.4s:

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





## References
1.	Gartner. (2024). Market Guide for Identity Governance and Administration. Gartner Research.

2.	IBM Security & Ponemon Institute. (2024). Cost of a Data Breach Report. https://www.ibm.com/reports/data-breach

3.	Cybersecurity Ventures. (2023). Cybersecurity Market Report. https://cybersecurityventures.com/cybersecurity-market-report/

4.	IBM. (2023). Cost of a Data Breach Report. Retrieved from: https://www.ibm.com/reports/data-breach 


5.	Ponemon Institute & Saviynt. (2023). The State of Identity and Access Management Maturity Report. Retrieved from: https://saviynt.com/resources/state-of-iam-maturity-2023 



