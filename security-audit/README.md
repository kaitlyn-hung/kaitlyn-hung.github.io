# Internal Security Audit

## Purpose
Audits help ensure that security checks are made, to monitor for threats, risks, or vulnerabilities that can affect an organization’s business continuity and critical assets. It is a review of an organization’s security controls, policies, and procedures against a set of expectations and can provide an overview of the risk and/or fines that the company might experience due to the current state of their security posture. 

---

## Scenario
Botium Toys is a growing U.S. toy company with one physical location serving as its main office, warehouse, and storefront. With a rapidly expanding consumer base and increasing digital operations, the IT manager has initiated an internal audit to strengthen security, maintain compliance, and support continued growth. The audit applies the NIST Cybersecurity Framework to assess risks, review existing controls, and ensure compliance with payment processing and E.U. business regulations.

*Scenario provided by the Google Cybersecurity Professional Certificate course.*

---

## Tasks
1️⃣ **Review the IT manager’s scope, goals, and risk assessment report.**

2️⃣ **Perform an internal audit by completing a controls and compliance checklist.**

3️⃣ **Explain checklist decisions.**

---

## Results
1️⃣ **Review the IT manager’s scope, goals, and risk assessment report.**

<img width="730" height="500" alt="Screen Shot 2025-10-09 at 11 17 55 PM" src="https://github.com/user-attachments/assets/7b14d9c8-950c-4438-975b-3939263939dd" />

*Risk Assessment provided by the Google Cybersecurity Professional Certificate course.*  

<br>
<br>

2️⃣ **Perform an internal audit by completing a controls and compliance checklist.**

First, I'll define the control categories. The different control types are preventative, corrective, detective, and deterent. 
+ **Administrative/Managerial controls** consist of the policies and procedures around data management and employee responsibilities of an organization. 
+ **Technical controls** involve the use of firewalls, intrusion detection systems (IDS), intrusion prevention systems (IPS), antivirus (AV) products, and encryption, amongst many other solutions. 
+ **Physical/Operational controls** are used to protect access by unauthorized personnel to physical assets. Door locks, cabinet locks, surveillance cameras, badge readers, etc. are included.

| Control                |  Does Toys & Toys have this control in place? |
|------------------------| -------------------------------------------: |
|Least Privilege         |   No  |
|Disaster recovery plans |   No  |
|Password policies       |   No  |
|Firewall                |  Yes  |
|IDS                     |  No   |
|Backups                 |  No   |
|Antivirus software      |  Yes  |
|Encryption                                                    | No  |
|Locks (offices, storefront, warehouse)                        | Yes |
|Closed-circuit television (CCTV) surveillance                 | Yes |
|Fire detection/prevention (fire alarm, sprinkler system, etc.)| Yes |  

<br>
<br>


3️⃣  **Explain checklist decisions.**

**Explanation**<br>
According to the Risk Assessment provided, all employees have access to company and customer data, including PII/SPII, meaning Botium Toys is not implementing the principle of least privilege. The principle of least privilege reduces the misuse of data because it gives employees **only** the minimum level of access or permissions they need to perform their tasks.<br>

The existing password policy does not meet minimum password complexity policies, meaning malicious actors may gain unauthorized access using brute force or dictionary attack techniques.<br>

IDS has not been installed meaning suspicious system activity will not be promptly detected and alerted to the IT team.<br>

Encryption is not currently used which puts ingoing and outgoing data at risk. Data should be confidential, authentic, reliable, and only accessible to those authorized.<br>

Currently, there aren't any disaster recovery plans or backups in place.

