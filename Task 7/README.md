# Vulnerability Scanning with Nikto

## Project Overview
This project demonstrates how to perform a **web server vulnerability scan** using **Nikto**, an open-source web server scanner.  
The objective is to identify common **security vulnerabilities, misconfigurations, and exposed information** on a web server.

This project is part of a **cybersecurity internship task** and follows ethical and legal security testing practices.

---

## Objective
- To perform vulnerability scanning on a web server using Nikto
- To analyze and document potential security issues
- To understand common web server misconfigurations
- To practice professional security documentation

---

## Tool Used
- **Nikto**  
  - Open-source web server vulnerability scanner  
  - Pre-installed on Kali Linux  
  - Used for identifying:
    - Outdated software
    - Missing security headers
    - Insecure files and configurations

---

## Target Details
- **Hostname:** testphp.vulnweb.com  
- **IP Address:** 44.228.249.3  
- **Port:** 80 (HTTP)

**Legal Note:**  
The target is a **deliberately vulnerable web application** provided for **security testing and educational purposes**.

---

## Methodology
- Installed Nikto on a Linux system.
- Executed a vulnerability scan against the target web application.
- Saved the scan output for analysis.
- Reviewed the findings to understand security risks and misconfigurations.
- Documented security impact and remediation recommendations.

---

## Scan Command Used
```bash
nikto -h http://testphp.vulnweb.com
```
---

## Key Findings
- Web server version (nginx/1.19.0) is exposed
- The web server discloses backend technology through the X-Powered-By header.
- Security headers such as X-Frame-Options and X-Content-Type-Options are missing.
- Cross-domain policy files (crossdomain.xml and clientaccesspolicy.xml) contain wildcard entries.
- These misconfigurations may increase the attack surface and assist attackers in reconnaissance and exploitation.

---

## Risk Severity Assessment

| Vulnerability | Severity |
|---------------|----------|
| Server version / technology disclosure | Medium |
| Missing X-Frame-Options header | Medium |
| Missing X-Content-Type-Options header | Low–Medium |
| crossdomain.xml wildcard entry | Medium |
| clientaccesspolicy.xml wildcard entry | Medium |

---

## Security Impaact
- Information disclosure can help attackers fingerprint server technologies.
- Missing anti-clickjacking protections may allow malicious framing attacks.
- Improper MIME handling can increase the risk of cross-site scripting (XSS).
- Overly permissive cross-domain policies may expose sensitive resources to untrusted domains.
- Information leakage
- Increased attack surface
- Clickjacking attacks
- Cross-site data access

---  

## Limitations
Nikto primarily detects known web server misconfigurations and does not exploit vulnerabilities. Manual testing and additional security tools are required for a comprehensive security assessment.

---

## Demo Video
A short demonstration showing how to perform a basic network scan using Nmap:
https://drive.google.com/file/d/1ZFkhnSGBL3ZUaEH8DgBgg9M3n74wVAkK/view?usp=sharing

---

## Conclusion
This project demonstrates the use of Nikto for identifying common web server vulnerabilities. Proper interpretation of scan results and timely remediation can significantly reduce security risks and strengthen web application defenses.



