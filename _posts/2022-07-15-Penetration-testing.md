---
title:  "Penetration Testing"
layout: post
---

Conducted both external and internal penetration tests of Rekall corporations (a simulated company) networks and systems. The purpose of this engagement was to assess the network security and identify potential security flaws by utilising industry-accepted testing methodology and best practices.
 
### I focused on the following:

Determining what system-level vulnerabilities could be discovered and exploited with no prior knowledge of the environment or notification to administrators.
Exploiting vulnerabilities found and accessing confidential information that may be stored on systems.
Documenting and reporting on all findings.

All tests took into consideration the actual business processes implemented by the systems and their potential threats. Therefore, the results of this assessment reflect a realistic picture of the actual exposure levels to online attackers. This document contains the results of that assessment.
 
### Assessment objective
 
The primary goal of this assessment was to provide an analysis of security flaws present in Rekall’s web applications, networks, and systems. This assessment was conducted to identify exploitable vulnerabilities and provide actionable recommendations on how to remediate the vulnerabilities, providing a greater level of security for the environment.

I used proven vulnerability testing methodology to assess all relevant web applications, networks, and systems in scope. 

### Rekall outlined the following objectives:

* Find and exfiltrate any sensitive information within the domain.
* Escalate privileges.
* Compromise several machines

### Penetration methodology

### Reconnaissance

I began with an initial assessment by checking for any passive (open source) data that may assist performing active recon using tools such as Nmap and Bloodhound.

### Identification of vulnerabilities and services

Used a mixture of custom, private, and public tools such as Metasploit, hashcat, and Nmap to gain perspective of the network security. These methods provide Rekall with an understanding of the risks that threaten its information, and also the strengths and weaknesses of the current controls protecting those systems. The results were achieved by mapping the network architecture, identifying hosts and services, enumerating network and system-level vulnerabilities, attempting to discover unexpected hosts within the environment, and eliminating false positives that might have arisen from scanning. 

### Vulnerability scanning

Manually tested each identified vulnerability and used automated tools to exploit these issues. Exploitation of a vulnerability is defined as any action I performed that resulted in me gaining unauthorised access to the system or potentially sensitive data.

### Reporting

Once exploitation was completed and all objectives had been completed, I drafted a report as a final deliverable to the customer. The penetration testing report for Rekall corporation can be seen [here](/Pentest.pdf).
