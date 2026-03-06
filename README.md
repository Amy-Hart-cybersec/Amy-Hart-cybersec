# Hello, I'm Amy


I am CompTIA Security+ certified and am continuing my cybersecurity studies at Moorpark College. I'm passionate about continuous learning, creative problem-solving, and contributing to mission-driven work.

## Objective

Aspiring cybersecurity professional with 10 years of experience working across industries, including Fortune 500 companies. Hands-on lab experience in threat detection, SIEM, endpoint monitoring, and digital forensics complements my strong analytical and problem-solving skills. Committed to protecting organizations from evolving cyber threats while continuously learning across technical and strategic domains.

## Home Lab Projects

**GRC Mini Risk Assessment Report**

Fictional Organization: Miller & Miller Marketing Firm (10 employees)

1.	Laptops (10)
a.	Threats and vulnerabilities include theft, malware, data loss, ransomware, lost/stolen device without encryption, unauthorized USB device use

b.	Risk: High

c.	Controls: Asset tagging, full disk encryption (Bitlocker/FileVault), EDR, automatic patching, remote wipe capability, screen lock policy, USB restrictions

2.	Monitors (10)

a.	Threats and vulnerabilities include theft

b.	Risk: Low

3.	Outlook (10 accounts)

a.	Threats and vulnerabilities include fraudulent wire transfer, payroll diversion fraud, phishing and malware, data loss, credential abuse, external email warning banners, and ransomware

b.	Risk: High

c.	Controls: Security awareness training, MFA requirements, conditional access policies, email archiving/retention policy, anti-phishing policies, and DMARC/SPF/DKIM enforcement

4.	Website

a.	Threats and vulnerabilities include malicious redirect and domain hijacking

b.	Risk: Low 

5.	Slack account

a.	Threats and vulnerabilities include data loss 

b.	Risk: Medium

c.	Controls: SSO with MFA, message retention policy, limiting third-party app approvals, and session timeout

6.	QuickBooks account

a.	Threats and vulnerabilities include vendor/ACH fraud, data loss, credential abuse, and ransomware

b.	Risk: High

c.	Controls: role-based access control list, principle of least privilege, separation of duties, MFA, backing up data, IP restriction (if available), transaction approval workflows, and audit log review

7.	Dropbox account

a.	Threats and vulnerabilities include misconfigured public link sharing, data loss, credential abuse, and ransomware

b.	Risk: High

c.	Controls: Requiring MFA, backing up data, DLP policies, link expiration policies, file activity monitoring, and device approvals requirement

8.	Physical office space

a.	Threats and vulnerabilities include equipment theft, fire, water damage, and power outage

b.	Risk: Medium

c.	Controls:  Alarm system, obscuring view of valuable like laptops and monitors via blinds, strategically placed cameras and lights, badge access, locked filing cabinets, clean desk policy, and document shredding policy

9.	Cloud-based VPN 

a.	Threats and vulnerabilities include compromised credentials, unauthorize access from person devices, misconfigured access policies, and over-provisioned user permissions

b.	Risk: Medium

c.	Controls: MFA required for VPN/access sessions, device posture checks, principle of least privilege regarding access policies, idle session timeout, and reviewing access logs periodically

**Phishing Analysis and Email Authentication Audit**

**Objective**
In this technical lab, I performed a forensic analysis of a suspicious email to validate sender authenticity. While the message bypassed basic filters by utilizing legitimate bulk-mailing infrastructure, I identified a Domain Alignment Failure through manual header triage. My analysis confirmed the message was a brand impersonation attempt, which was mitigated by the organization's DMARC policy.

**Tools Used**

Gmail Source View: For raw header extraction.

Cisco Talos Intelligence: For IP reputation and threat intelligence.

**Methodology**

Header Extraction: Accessed the "Original Source" of a suspicious email to review the hop-by-hop delivery path.

Security Protocol Audit: Analyzed the three pillars of email security:

SPF (Sender Policy Framework): Verified if the sending IP was authorized by the domain's owner.

DKIM (DomainKeys Identified Mail): Checked for digital signatures to ensure the message was not altered in transit.

DMARC: Verified the domain's policy for handling failed SPF/DKIM checks.

Threat Intelligence Mapping: Extracted the originating IP address from the Received: header and cross-referenced it with Cisco Talos.

| Metric | Value | Status | Analysis |
| :--- | :--- | :--- | :--- |
| **From Address** | `admin@aaapathfinds.com` | **Impersonated** | The identity the attacker is trying to impersonate to deceive the end-user. |
| **Return-Path** | `errors-[useremail]@rch003.net` | **Mismatch** | The real source of the email. There is a domain mismatch. |
| **SPF** | `PASS` | Valid | The sending server at `rch003.net` is authorized to send mail for its own domain. |
| **DKIM** | `PASS` | Valid | The message was digitally signed by the `rch003.net` server. |
| **DMARC** | `FAIL` |**Non-Alignment** | DMARC failed because the "From" domain and "DKIM/SPF" domains are not aligned. |

## Takeaway

Even though SPF and DKIM technically passed, they passed for the service provider, not the impersonated brand. The attacker's tactic indicates trying to leverage higher reputation bulk-mailers to bypass filters that don't check for DMARC alignment. I identified the phishing attempt by performing a manual header audit. The use of Variable Envelope Return Path (VERP) in the Return-Path header further confirms the use of automated bulk-mailer software, an indicator of high-volume phishing campaigns. Successfully triaged the threat without interacting with embedded links or attachments.

## Mitigation Efforts
1. **Triage:** Identified the mismatch between the Display Domain and the Signing Domain.
2. **Reputation Check:** Extracted the originating IP for cross-referencing with threat intelligence databases (Cisco Talos). The result was Neutral.
3. **Reporting:** Verified that the local DMARC policy correctly routed the message to the Spam folder.

## Skills


| Skill                                         | Associated Lab             |
|-----------------------------------------------|----------------------------|
| Threat Detection & Analysis                   | [Intro to Cyber Threat Intel](https://tryhackme.com/room/cyberthreatintel)
| Network Traffic Analysis                      | [Traffic Analysis Essentials](https://tryhackme.com/room/trafficanalysisessentials)
| PCAP Analysis                                 | [Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics)
| Log Analysis & SIEM Operations                | [Introduction to SIEM](https://tryhackme.com/room/introtosiem)
| Log Analysis & SIEM Operations                | [Introduction to Log Analysis](https://tryhackme.com/room/introtologanalysis)
| Security Monitoring & Incident Response       | [Auditing and Monitoring](https://tryhackme.com/room/auditingandmonitoringse)
| Microsoft Sentinel                            | [MS Sentinel: Introduction](https://tryhackme.com/room/sentinelintroduction)
| Splunk                                        | [Splunk: The Basics](https://tryhackme.com/room/splunk101)
| Malware Analysis                              | [Intro to Malware Analysis](https://tryhackme.com/room/intromalwareanalysis)
| Digital Forensics                             | [DFIR: An Introduction](https://tryhackme.com/room/introductoryroomdfirmodule)
| Digital Forensics                             | [Windows Forensics 1](https://tryhackme.com/room/windowsforensics1)
| Digital Forensics                             | [Linux Forensics](https://tryhackme.com/room/linuxforensics)
| MITRE ATT&CK Mapping                          | [MITRE](https://tryhackme.com/room/mitre)
| Threat Hunting                                | [Eviction](https://tryhackme.com/room/eviction)
| Endpoint Security & EDR                       | [Intro to Endpoint Security](https://tryhackme.com/room/introtoendpointsecurity)
| Sysmon                                        | [Sysmon](https://tryhackme.com/room/sysmon)
| Velociraptor                                  | [Velociraptor](https://tryhackme.com/room/velociraptorhp)
| Phishing Analysis                             | [Phishing Analysis Fundamentals](https://tryhackme.com/room/phishingemails1tryoe)
| Phishing Analysis                             | [Phishing Emails in Action](https://tryhackme.com/room/phishingemails2rytmuv)
| Detection Engineering                         | [Intro to Detection Engineering](https://tryhackme.com/room/introtodetectionengineering)
| Threat Hunting                                | [Hunt Me I: Payment Collectors](https://tryhackme.com/room/paymentcollectors)
| Threat Hunting                                | [Boogeyman 1](https://tryhackme.com/room/boogeyman1)

## Certifications
CompTIA Security+ Certified

