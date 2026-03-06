
IT Compliance & Risk Assessment Lab | Governance, Risk & Compliance (GRC) Simulation

Executive Summary

This lab simulates the role of an IT Compliance or Governance, Risk & Compliance (GRC) Analyst for a small healthcare organization, “ABC Health Services.” The project demonstrates the practical application of IT governance, risk assessment, and compliance processes within an environment lacking formalized security controls.

The objectives of this lab were to identify vulnerabilities, evaluate compliance gaps, implement technical and administrative controls, and develop foundational governance documentation aligned with industry standards such as the NIST Cybersecurity Framework and HIPAA security concepts.

Key outcomes include:

  Conducting a structured risk assessment and developing a risk matrix.

  Identifying technical and operational security gaps.

  Implementing security controls mapped to NIST CSF functions and categories.

  Creating essential policy documentation: Access Control, Password, Acceptable Use, Data Protection, Incident Response, and User Provisioning/Deprovisioning.

  Applying governance best practices to reduce operational risk, strengthen access management, and support compliance auditing.

  This lab bridges operational management expertise with technical GRC skills, providing a strong foundation for roles in IT governance, compliance, and cybersecurity risk management.

Project Overview

Scenario:
ABC Health Services, a small healthcare organization with 25 employees, requested a basic IT risk assessment and compliance review to evaluate its security posture and ensure the protection of sensitive patient data.

Environment Highlights:

  Windows-based endpoints

  No formalized IT security policies

  No structured access control or onboarding/offboarding processes

  Sensitive patient data (PHI) stored locally

Lab Objectives:

  Conduct a comprehensive IT risk assessment

  Identify threats, vulnerabilities, and gaps

  Evaluate impact and likelihood to prioritize risks

  Create a risk matrix and document mitigation strategies

  Develop core security policies and governance documentation

  Align implemented controls with industry best practices
  
🛠 Frameworks & Concepts Referenced

  NIST Cybersecurity Framework

  CIA Triad (Confidentiality, Integrity, Availability)

  Least Privilege Principle

  Role-Based Access Control (RBAC)

  Basic HIPAA security concepts

  Risk Management lifecycle

🔍 Step 1: Asset Identification

  Identified critical assets:

  Domain Controller

  Employee workstations

  Patient data (PHI)

  Email system

  Network router/firewall

  Backup storage

⚠️ Step 2: Threat & Vulnerability Identification

  Identified potential risks:

  Weak password policies

  Excessive administrative privileges

  No multi-factor authentication

  Unpatched systems

  Lack of centralized logging

  Inconsistent onboarding/offboarding processes

  No documented incident response plan

📊 Step 3: Risk Assessment Matrix

  Each risk was evaluated using:

  Likelihood (Low / Medium / High)

  Impact (Low / Medium / High)

Overall Risk Rating


| Risk ID | Risk Description                                                                                                             | Impact | Likelihood | Risk Level | Mitigation / Control Implemented                                                                                                           | Status    |
| ------- | ---------------------------------------------------------------------------------------------------------------------------- | ------ | ---------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------ | --------- |
| R-01    | Weak password policies could allow attackers to guess or brute-force user credentials.                                       | High   | Medium     | High       | Enforced password complexity, minimum length, and expiration policies through Active Directory Group Policy.                               | Mitigated |
| R-02    | Excessive user privileges could allow standard users to perform administrative actions or modify system configurations.      | High   | Medium     | High       | Implemented least privilege by restricting administrative rights and validating that standard users cannot perform administrative actions. | Mitigated |
| R-03    | Unrestricted inbound firewall rules could allow unauthorized network access to the endpoint.                                 | Medium | Medium     | Medium     | Reviewed inbound firewall rules and disabled unnecessary services such as Remote Assistance and consumer networking services.              | Mitigated |
| R-04    | Unnecessary Windows services running in the background could increase the system’s attack surface.                           | Medium | Medium     | Medium     | Disabled non-essential services such as Remote Registry and Routing and Remote Access.                                                     | Mitigated |
| R-05    | Lack of endpoint security controls could allow unauthorized changes to system configurations.                                | Medium | Low        | Low        | Applied local security policy hardening to enforce security settings and system protections.                                               | Mitigated |
| R-06    | Improper network configuration could allow systems to operate without proper domain authentication and security enforcement. | Medium | Medium     | Medium     | Implemented proper domain connectivity and validated network communication through DNS resolution and domain authentication.               | Mitigated |

Gap Analysis

The environment was evaluated against common cybersecurity best practices aligned with the NIST Cybersecurity Framework. Several configuration and security control gaps were identified prior to implementing mitigation measures.

| Control Area                    | Current State (Before Mitigation)                                            | Identified Gap                                                   | Risk Impact                                                           | Recommended Action                                              |
| ------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------- |
| Password Security               | Default password policies were in place                                      | Password complexity and minimum length requirements not enforced | Weak passwords could allow brute-force or credential guessing attacks | Implement strong password policies through Group Policy         |
| Privileged Access Management    | Standard users could potentially attempt administrative actions              | Lack of strict least privilege enforcement                       | Unauthorized system changes or privilege escalation                   | Restrict administrative privileges to authorized accounts only  |
| Firewall Configuration          | Multiple inbound firewall rules enabled by default                           | Non-essential services exposed through firewall                  | Increased attack surface for unauthorized network access              | Disable unnecessary inbound firewall rules                      |
| Service Hardening               | Several Windows services enabled that were not required for system operation | Unnecessary services increase attack surface                     | Potential exploitation of vulnerable services                         | Disable non-essential services such as Remote Registry          |
| Endpoint Security Configuration | Default local security policy settings                                       | Security policies not hardened for enterprise environments       | Reduced endpoint protection and increased risk of misconfiguration    | Apply security hardening through Local Security Policy          |
| Network Configuration           | Network connectivity initially misconfigured between systems                 | Lack of proper DNS and domain communication configuration        | Systems unable to properly authenticate within the domain             | Configure proper DNS settings and validate network connectivity |



🛡 Step 4: Control Recommendations


Control Mapping Methodology

Security controls implemented during this lab were mapped to functions and categories from the NIST Cybersecurity Framework to demonstrate how technical security configurations support broader cybersecurity risk management practices.

Control Mapping to NIST Cybersecurity Framework


| Risk ID | Security Control Implemented                                                         | NIST CSF Function | NIST CSF Category                            | Implementation Evidence                                           |
| ------- | ------------------------------------------------------------------------------------ | ----------------- | -------------------------------------------- | ----------------------------------------------------------------- |
| R-01    | Enforced password complexity and minimum password length through Group Policy        | Protect           | PR.AC – Identity Management & Access Control | Screenshot of Domain Password Policy Configuration                |
| R-02    | Applied least privilege by restricting standard users from administrative privileges | Protect           | PR.AC – Identity Management & Access Control | Screenshot showing administrative action denied for standard user |
| R-03    | Hardened endpoint firewall by disabling non-essential inbound rules                  | Protect           | PR.IP – Protective Technology                | Screenshot of disabled inbound firewall rules                     |
| R-04    | Disabled unnecessary Windows services to reduce attack surface                       | Protect           | PR.IP – Protective Technology                | Screenshot of disabled services in Services Manager               |
| R-05    | Applied local security policy hardening on endpoint system                           | Protect           | PR.IP – Configuration Management             | Screenshot of Local Security Policy configuration                 |
| R-06    | Verified domain authentication and DNS communication between systems                 | Detect            | DE.CM – Security Continuous Monitoring       | Screenshot of successful ping and nslookup validation             |


📄 Step 5: Policy Development

Created sample documentation including:

Access Control Policy
  Access to organizational systems must be restricted to authorized users and managed according to the principle of least privilege. All users must be assigned unique accounts, and administrative privileges shall only be granted to personnel with approved   administrative responsibilities. User permissions must be reviewed periodically to ensure access levels remain appropriate and aligned with job functions.

Password Policy
  Minimum 12 characters with uppercase, lowercase, numbers, and special characters

  Change passwords every 90 days; cannot reuse the last 5

  Accounts lock after 5 failed login attempts

  Multi-Factor Authentication (MFA) required for remote and privileged accounts

  Do not share or store passwords in plain text; use approved password managers

Acceptable Use Policy
  All organizational systems, devices, and networks are for official business purposes only.

  Users must protect login credentials and not share accounts.

  No unauthorized software or hardware may be installed on company devices.

  Prohibited activities include:

Accessing inappropriate or illegal content

Attempting to bypass security controls

Using company resources for personal financial gain or political purposes

Violations may result in access restrictions or disciplinary action.

Incident Response Outline
  Purpose:
    To define the process for detecting, reporting, and responding to security incidents to minimize impact and restore normal operations quickly.

  Steps:

Identification – Detect and confirm potential security incidents.

Containment – Limit the scope and impact of the incident.

Eradication – Remove the root cause and affected systems or accounts.

Recovery – Restore systems to normal operations and verify functionality.

Lessons Learned – Analyze the incident, update policies, and improve controls.

  Reporting:

    All incidents must be reported to IT/security immediately.

    Document incident details including time, scope, and actions taken.

Data Protection Policy
  
  All sensitive and confidential data must be stored securely and accessed only by authorized personnel.

  Data must be encrypted in transit and at rest whenever possible.

  Regular backups must be maintained to prevent data loss.

  Personal or customer data must be handled in accordance with privacy regulations (e.g., HIPAA, GDPR).

  Unauthorized sharing, copying, or disclosure of data is prohibited.

  Employees must report data breaches or suspected incidents immediately.
  
User Provisioning & Deprovisioning Procedure
  Provisioning: 
    Access to systems and applications is granted based on job role and least privilege.

    All new accounts must be approved by management and documented.

  Deprovisioning:

    Accounts for departing employees, contractors, or role changes must be disabled or removed immediately.

    Access rights must be reviewed regularly to ensure compliance with least privilege principles.

  Account Reviews:

    Periodic audits are conducted to verify active accounts and prevent unauthorized access.

🔐 Security Principles Applied

Defense in Depth

Risk Prioritization

Preventative vs Detective Controls

Administrative vs Technical Controls

Governance Documentation

📚 Key Takeaways

Many organizations lack formalized documentation

Governance documentation reduces operational risk

Risk assessment must consider both technical and human factors

Access management is one of the most critical compliance controls

Structured onboarding/offboarding reduces insider risk

🚀 Future Improvements

Map controls directly to NIST categories

Simulate audit preparation checklist

Develop a Business Continuity Plan (BCP)

Create formal risk register spreadsheet
