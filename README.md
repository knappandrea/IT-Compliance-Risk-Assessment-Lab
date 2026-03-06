
IT Compliance & Risk Assessment Lab
Governance, Risk & Compliance (GRC) Simulation

📌 Project Overview

This project simulates the role of an IT Compliance or Governance, Risk & Compliance (GRC) Analyst within a small organization. The lab focuses on identifying security risks, evaluating compliance gaps, and developing security policies aligned with industry best practices.

The objective of this lab was to apply risk assessment methodology, document security controls, and create foundational governance documentation similar to what is required in regulated industries such as healthcare and finance.

🏢 Scenario

A fictional healthcare organization (“ABC Health Services”) requested a basic IT risk assessment and compliance review to evaluate its security posture and ensure protection of sensitive data.

The organization:

Uses Windows endpoints

Stores sensitive patient data

Has 25 employees

Has no formalized IT security policies

Lacks structured access control procedures

🎯 Objectives

Conduct a basic IT risk assessment

Identify vulnerabilities and potential threats

Evaluate impact and likelihood

Create a risk matrix

Develop security policy documentation

Recommend mitigation strategies

Align controls with industry best practices

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

Password Policy

Acceptable Use Policy

Incident Response Outline

Data Protection Policy

User Provisioning & Deprovisioning Procedure

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
