# Active Reconnaissance and Vulnerability Scanning

## Project Overview

This project demonstrates active reconnaissance and vulnerability assessment techniques performed within a controlled and authorized lab environment. The objective is to identify open ports, running services, potential vulnerabilities, and security risks using industry-standard cybersecurity tools.

The project focuses on ethical security testing practices and vulnerability identification to strengthen system security.

---

## Objectives

- Perform host discovery
- Enumerate open ports and services
- Identify operating systems and software versions
- Conduct vulnerability scanning
- Document security findings
- Assess risks and recommend mitigations

---

## Tools Used

- Nmap
- Nikto
- OpenVAS / Greenbone
- Kali Linux
- VirtualBox / VMware
- Metasploitable2 / DVWA (Test Target)

---

## Lab Setup

Environment:

```
Kali Linux VM (Attacker Machine)
        ↓
Target Test System
(Metasploitable2 / DVWA)
```

Testing was performed only on authorized systems within a safe laboratory environment.

---

## Reconnaissance Phase

### Host Discovery

Command:

```bash
nmap -sn 192.168.56.0/24
```

Purpose:

- Identify active hosts
- Discover reachable systems

---

### Port Enumeration

Command:

```bash
nmap <Target-IP>
```

Purpose:

- Detect open ports
- Identify exposed services

Example:

```
22/tcp open ssh
80/tcp open http
3306/tcp open mysql
```

---

### Service Enumeration

Command:

```bash
nmap -sV <Target-IP>
```

Purpose:

- Detect service versions
- Identify software running on ports

Example:

```
22/tcp open ssh OpenSSH 8.2

80/tcp open http Apache 2.4.41
```

---

### Operating System Detection

Command:

```bash
nmap -O <Target-IP>
```

Purpose:

- Identify target operating system

---

### Aggressive Scan

Command:

```bash
nmap -A <Target-IP>
```

Purpose:

- Service detection
- Version detection
- OS fingerprinting
- Script scanning

---

## Vulnerability Assessment

### Nikto Scan

Command:

```bash
nikto -h http://<Target-IP>
```

Purpose:

- Detect web vulnerabilities
- Identify outdated software
- Find insecure configurations

Possible Findings:

- Missing security headers
- Directory listing enabled
- Outdated web server software

---

### OpenVAS Scan

Procedure:

1. Configure target system
2. Create scan task
3. Execute vulnerability scan
4. Export findings report

Example vulnerabilities:

- Weak SSL configuration
- Outdated software
- Open database exposure

---

## Findings Summary

| Finding | Risk |
|----------|------|
| Open SSH Port | Unauthorized access risk |
| Exposed HTTP Service | Web attack surface |
| Database Port Accessible | Data exposure |
| Outdated Services | Known vulnerabilities |

---

## Security Recommendations

- Close unused ports
- Restrict SSH access
- Update outdated software
- Apply security patches
- Configure firewall rules
- Disable unnecessary services
- Add security headers

---

## Skills Demonstrated

- Network Reconnaissance
- Port Enumeration
- Service Detection
- Vulnerability Scanning
- Security Risk Assessment
- Security Documentation
- Ethical Hacking Fundamentals

---

## Project Structure

```

Active-Recon-Vulnerability-Scanning/
│
├── nmap_report.txt
├── nikto_report.txt
├── openvas_report.pdf
├── screenshots/
├── findings_report.pdf
└── README.md

```

---

## Learning Outcomes

This project strengthened practical knowledge in:

- Vulnerability assessment methodology
- Network reconnaissance techniques
- Risk identification
- Security hardening concepts
- Defensive cybersecurity practices

---

## Ethical Notice

This project was conducted only in a safe and authorized environment. Vulnerability scanning and reconnaissance should never be performed on systems without explicit permission.

---

## Author

**Animesh Tiwari**

Cybersecurity Enthusiast | Python Learner | AI & Security Explorer
