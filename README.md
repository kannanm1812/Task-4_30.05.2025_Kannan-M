# Task-4_30.05.2025_Kannan-M
Task 4 Dated 30.05.2025 submitted by Kannan M
# 🔐 Task 4: Setup and Use a Firewall on Kali Linux


### 🎯 Objective:
Configure and test basic firewall rules to allow or block network traffic using UFW on Kali Linux.

---

## 💻 Environment 1:
- OS: Kali Linux  
- Firewall Tool: UFW (Uncomplicated Firewall)

---

## ⚙️ Steps Performed:

### 1. **Installed UFW (if not already installed)**
```bash
sudo apt update
sudo apt install ufw
```

### 2. **Checked UFW status**
```bash
sudo ufw status
```

### 3. **Enabled UFW**
```bash
sudo ufw enable
```

### 4. **Listed current firewall rules**
```bash
sudo ufw status numbered
```

### 5. **Blocked inbound traffic on port 23 (Telnet)**
```bash
sudo ufw deny 23
```

### 6. **Allowed SSH on port 22**
```bash
sudo ufw allow 22
```

### 7. **Tested firewall rules**
- Verified Telnet block using:
```bash
telnet localhost 23
```
- Scanned ports using:
```bash
nmap localhost
```

### 8. **Deleted test block rule (cleanup)**
```bash
sudo ufw delete deny 23
```

## 💻 Environment 2:
- OS: Windows 10 / 11  
- Firewall Tool: Windows Defender Firewall (GUI)

---

## ⚙️ Steps Performed:

### 1. **Opened Windows Firewall**
- Accessed it via Control Panel or by running `wf.msc` from the Run dialog (Win + R).

### 2. **Viewed existing inbound rules**
- Navigated to **Inbound Rules** to see current configurations.

### 3. **Blocked inbound traffic on port 23 (Telnet)**
- Created a new rule:
  - Rule Type: **Port**
  - Protocol: **TCP**
  - Port: **23**
  - Action: **Block the connection**
  - Profile: **All**
  - Name: **Block Telnet**

### 4. **Allowed SSH on port 22**
- Created another rule to **allow** TCP traffic on port **22** (if SSH service is running).

### 5. **Tested the rule**
- Verified Telnet was blocked using a Telnet client or port scanner.

### 6. **Deleted the Telnet rule (cleanup)**
- Located and deleted the **Block Telnet** rule from Inbound Rules.

---

## 🧾 Summary

The UFW firewall on Kali Linux was successfully configured to:
- Block Telnet (port 23), preventing unencrypted access
- Allow SSH (port 22) for secure management

This showed how UFW can effectively filter and manage network traffic.


Windows Defender Firewall was successfully configured to:
- Block Telnet connections (port 23), which is an insecure protocol.
- Allow SSH (port 22) for secure connections if required.

---

## 📸 Screenshots

!screenshots of the terminal showing each step

!GUI screenshots of the steps performed in Windows Firewall.

---

## 📚 Key Learnings

- **Firewall**: A security tool that controls incoming and outgoing network traffic.
- **UFW**: A user-friendly command-line interface for managing iptables.
- **Ports**: Logical connection points for network services (e.g., 22 for SSH, 23 for Telnet).
- **Inbound/Outbound Rules**: Determine traffic direction and access.

---

## 📁 Files in this Repo
- `README.md` – Summary of the task
- `/screenshots/` – Screenshots of the terminal and GUI

## 🔗 Submission

**GitHub Repo Link**: https://github.com/kannanm1812/Task-4_30.05.2025_Kannan-M.
**Submission Form**: https://docs.google.com/forms/u/0/d/e/1FAIpQLSe64ZYruA9GGLdeHn2_AMWLWvWfHiALtnfaWOwtcPXGpnKgJg/formResponse

---

## ✅ Task Completed
