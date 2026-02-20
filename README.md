# Hello, I'm Amy


I am CompTIA Security+ certified and am continuing my cybersecurity studies at Moorpark College. I'm passionate about continuous learning, creative problem-solving, and contributing to mission-driven work.

## Objective

Aspiring cybersecurity professional with 10 years of experience working across industries, including Fortune 500 companies. Hands-on lab experience in threat detection, SIEM, endpoint monitoring, and digital forensics complements my strong analytical and problem-solving skills. Committed to protecting organizations from evolving cyber threats while continuously learning across technical and strategic domains.

## Home Lab Projects

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
| **DMARC** | `FAIL` |**Non-Alignment:** DMARC failed because the "From" domain and "DKIM/SPF" domains are not aligned. |

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

