# 🛡️ Penetration Testing Lab Portfolio

Welcome to my hands-on penetration testing repository. This collection of exploit walkthroughs and screenshots showcases my practical skills in identifying, exploiting, and documenting vulnerabilities using tools like:

- Kali Linux  
- Metasploit  
- Nmap  
- Netcat  
- Manual exploitation  

---

## 📚 Included Labs

- ✅ [vsFTPd 2.3.4 Backdoor](#vsftpd-234-backdoor)
- ⏳ Samba trans2 buffer overflow *(coming soon)*
- ⏳ TWiki remote code execution *(coming soon)*

---

## 🎯 Goal

To demonstrate real-world offensive security techniques using isolated test environments and intentionally vulnerable machines.

---

## 📂 vsFTPd 2.3.4 Backdoor

The `vsFTPd 2.3.4` service contains a malicious backdoor triggered when a username ends with a `:)`.

---

### 🔎 Nmap Scan

We start with a basic service and version detection scan:

```bash
nmap -A -T4 192.168.56.101

