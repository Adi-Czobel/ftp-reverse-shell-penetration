# FTP & Reverse Shell Penetration Testing Report

This project documents a hands-on penetration test targeting a misconfigured FTP service and HTTP web app to gain root access through a reverse shell exploit.

## 📄 PDF Report

👉 [Click here to read the full report](./CSE_Lab_13.pdf)

## 🔍 Summary

- **Target IP:** 10.43.10.159  
- **Attack Methods:**
  - Exploited anonymous FTP access (Port 9000)
  - Logged into web interface using leaked credentials
  - Uploaded a PHP reverse shell and gained remote control
  - Used `sudo vim` to escalate privileges to root

## 🧰 Tools Used

- Nmap  
- DirBuster  
- Netcat  
- FTP client  
- Firefox

## 🚨 Key Vulnerabilities

| Vulnerability            | Severity | Summary                                           |
|--------------------------|----------|---------------------------------------------------|
| Anonymous FTP Access     | Critical | Exposed credentials for web login                |
| Reverse Shell Upload     | High     | Executed remote shell to attacker’s machine      |
| Privilege Escalation     | High     | Root gained via misconfigured sudo permissions   |
| Open Port Enumeration    | Medium   | Increased attack surface (HTTP, FTP, SSH)        |

## ✅ Recommendations

- Disable anonymous FTP access  
- Validate all file uploads  
- Audit `sudo` access for least privilege  
- Close unnecessary ports

---

## Author

**Adi Czobel**  
UBNetDef Student – University at Buffalo  
April 2025
