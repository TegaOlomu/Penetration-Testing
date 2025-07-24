# Penetration-Testing
This repository contains the deliverables from a simulated internal penetration test conducted for ZeroHealth Corp in July 2025.

---

## 🎯 Objectives

- Identify exploitable vulnerabilities across internal services.
- Demonstrate proof-of-concept exploits in a controlled environment.
- Assess the potential business and compliance risks.
- Recommend actionable remediation steps.

---

## 📃 Scope & Authorization

This project was conducted under a defined and approved scope, as per the documents below:

- [Scope of Work](https://drive.google.com/file/d/15PIaIymt_s1wH_ec-ExN987LAgU9YHWB/view?usp=sharing): Details the rules of engagement, objectives, and systems included in the penetration test.
- [Authorization Document](https://drive.google.com/file/d/1T3xoCG1534ZFW_22UtCvu5jh6TjRfMjS/view?usp=sharing): Provides explicit permission from ZeroHealth Corp's CISO for penetration testing activities, ensuring legal and ethical compliance.

These documents confirm that all testing activities were authorized and executed within the agreed boundaries.

---
## 📁 Full Contents

| File | Description |
|-------------|-------------|
| [Final Report](https://drive.google.com/file/d/1bpzBmXsXTkm4O3eRFWLMjr3iBE90TLl3/view?usp=sharing) | Complete formal penetration testing report in PDF format. |
| [Slides](https://drive.google.com/file/d/1HRHGi1pA8E-m6XSkXcFXW1uQ5QO6bz9B/view?usp=drive_link) | Executive-level presentation summarizing findings and recommendations. |

---

## 🛠️ Tools & Technologies Used

- **Kali Linux**
- **Metasploit Framework**
- **Metasploitable 2**
- **Nmap**, **Nikto**
- **Burp Suite**, **OWASP ZAP**
- **TheHarvester**, **SearchSploit**
- **Manual Enumeration** (`netcat`, `cat`, `ls`, etc.)

---

## 🔍 Key Results

- 17 vulnerabilities identified (5 High/Critical)
- Full system compromise via Samba, UnrealIRCd, and distccd
- Extracted sensitive credentials and data
- XSS Reflected attack on DVWA using Burp Suite

---

## 🔐 Remediation Highlights

- Apply security patches to Samba, distccd, Apache Tomcat
- Disable outdated services: FTP, Telnet, bind shells
- Implement network segmentation and port restrictions
- Conduct employee phishing and password training

---

## 📅 Engagement Timeline

| Phase | Dates |
|-------|-------|
| Planning & Scoping | July 5, 2025 |
| Testing & Exploitation | July 6–10, 2025 |
| Post-Exploitation | July 11, 2025 |
| Final Reporting | July 12, 2025 |

---

# Exploits Used Per Vulnerability

| Vulnerability                | Port | Tool/Exploit Module                                 | Outcome |
|-----------------------------|------|------------------------------------------------------|---------|
| Samba RPC Buffer Overflow          | 139  | `exploit/multi/samba/usermap_script`                | Shell access |
| UnrealIRCd Backdoor         | 6667 | `exploit/unix/irc/unreal_ircd_3281_backdoor`        | Root shell |
| Apache Tomcat WAR Deployment    | 8180 | `exploit/multi/http/tomcat_mgr_upload`              | Web app admin takeover |
| distccd Remote Command Execution   | 3632 | `exploit/unix/misc/distcc_exec`                     | Arbitrary command execution |
| Metasploitable Root Shell Backdoor        | 1524  | Netcat    | Unrestricted root |

---


## 📜 License & Ethical Statement

This repository is for educational and authorized simulation purposes only. No real systems were harmed. All testing was performed within a safe lab environment using vulnerable machines (Metasploitable2).

---

*Prepared by:*  
**Tega Olomu**  
Cybersecurity Analyst | July 2025  
