# 🪟 Windows Command Line (CMD) – Essential Commands Guide

A categorized reference of **commonly used Windows CMD commands** for navigation, networking, system repair, security, power management, and troubleshooting.

---

## 📁 Directory & File Management Commands

### 📌 `cd .`

#### Description:

- Refers to the **current directory**.

```cmd
cd .
```

#### Where & When Used:

- Used in scripts
- Confirms current working directory

### 📌 `cd ..`

#### Description:

- Moves one level up in the directory tree.
```cmd
cd ..
```

#### Where & When Used:

- Directory navigation
- File system traversal

### 📌 `cd <path>`

#### Description:

- Changes directory to a specified path.
```cmd
cd C:\Users\Public
cd D:\Projects
```

#### Where & When Used:

- Navigating folders
- Running commands inside a specific directory

### 📌 `mkdir`

#### Description:

- Creates a new directory.
```cmd
mkdir NewFolder
```

#### Where & When Used:

- Organizing files
- Creating project folders

---

## 🌐 Network & Internet Commands

### 📌 `ipconfig`

#### Description:

- Displays IP configuration details.
```cmd
ipconfig
```

#### Where & When Used:

- Network diagnostics
- Checking IP address

### 📌 `ipconfig /flushdns`

#### Description:

Clears the DNS resolver cache.
```cmd
ipconfig /flushdns
```

#### Where & When Used:

- Fix DNS issues
- Website loading problems

### 📌 `ipconfig /release`

#### Description:

- Releases current IP address.
```cmd
ipconfig /release
```

#### Where & When Used:

- Network reset
- DHCP troubleshooting

### 📌 `ipconfig /renew`

#### Description:

- Requests a new IP address from DHCP.
```cmd
ipconfig /renew
```

#### Where & When Used:

- After /release
- Fix connectivity issues

### 📌 `ping <website / IP>`

#### Description:

- Tests connectivity to a host.
```cmd
ping google.com
ping 8.8.8.8
```

#### Where & When Used:

- Internet connectivity testing
- Latency checking

### 📌 `tracert`

#### Description:

- Traces route packets take to a destination.
```cmd
tracert google.com
tracert 8.8.8.8
```

#### Where & When Used:

- Network troubleshooting
- Finding latency issues

### 📌 `nslookup`

#### Description:

- Queries DNS records.
```cmd
nslookup
nslookup google.com
```

#### Where & When Used:

- DNS troubleshooting
- Server lookup

### 📌 `netsh winsock reset`

#### Description:

- Resets Winsock catalog.

```cmd
netsh winsock reset
```

#### Where & When Used:

- Fix network corruption
- Internet issues after malware

### 📌 `netsh int ip reset`

#### Description:

- Resets TCP/IP stack.
```cmd
netsh int ip reset
```

#### Where & When Used:

- Severe network problems
- Network adapter issues

### 📌 `netsh wlan show wlanreport`

#### Description:

- Generates Wi-Fi diagnostics report.
```cmd
netsh wlan show wlanreport
```

#### Where & When Used:

- Wi-Fi connection debugging
- Network diagnostics

---

## 🖥️ System Information Commands

### 📌 `systeminfo`

#### Description:

- Displays detailed system information.
```cmd
systeminfo
```

#### Where & When Used:

- System auditing
- Hardware & OS details

### 📌 `sysinfo64`

#### Description:

- Displays system info (if Sysinternals installed).
```cmd
sysinfo64
```

#### Where & When Used:

- Advanced system diagnostics

---

## 🔧 Disk & File System Commands

### 📌 `chkdsk C: /r`

#### Description:

- Checks disk and recovers bad sectors.
```cmd
chkdsk C: /r
```

#### Where & When Used:

- Disk errors
- File corruption repair

### 📌 `cipher /w:D:`

#### Description:

- Securely wipes free space on a drive.
```cmd
cipher /w:D:
```

#### Where & When Used:

- Data privacy
- Secure deletion

### 📌 `cipher /e /s:D:\encrypted`

#### Description:

- Encrypts files and folders.
```cmd
cipher /e /s:D:\encrypted
```

#### Where & When Used:

- File security
- Sensitive data protection

---

## 🧠 Process & Task Management

### 📌 `tasklist`

#### Description:

- Displays running processes.
```cmd
tasklist
```

#### Where & When Used:

- Monitor active programs
- Debug high CPU usage

### 📌 `taskkill /f /t /pid <PID>`

#### Description:

- Force kills a process by PID.
```cmd
taskkill /f /t /pid 1234
```

#### Where & When Used:

- Kill frozen applications

### 📌 `taskkill /f /im cmd.exe`

#### Description:

- Terminates a process by name.
```cmd
taskkill /f /im cmd.exe
```

#### Where & When Used:

- Close specific programs

---

## 🛠️ System Repair & Health Commands

### 📌 `sfc /scannow`

#### Description:

- Scans and repairs system files.
```cmd
sfc /scannow
```

#### Where & When Used:

- Fix corrupted Windows files

### 📌 `dism /online /cleanup-image /scanhealth`

#### Description:

- Scans Windows image for corruption.
```cmd
dism /online /cleanup-image /scanhealth
```

#### Where & When Used:

- System diagnostics

### 📌 `dism /online /cleanup-image /restorehealth`

#### Description:

- Repairs Windows image.
```cmd
dism /online /cleanup-image /restorehealth
```

#### Where & When Used:

- Fix OS corruption

---

## 🔋 Power & Battery Commands

### 📌 `powercfg /energy`

#### Description:

- Analyzes system power efficiency.
```cmd
powercfg /energy
```

#### Where & When Used:

- Power optimization
- Laptop diagnostics

### 📌 `powercfg /batteryreport`

#### Description:

- Generates battery health report.
```cmd
powercfg /batteryreport
```

#### Where & When Used:

- Battery health monitoring

---

## 🚘 Driver Commands

### 📌 `driverquery`

#### Description:

- Lists installed drivers.
```cmd
driverquery
```

#### Where & When Used:

- Driver diagnostics

### 📌 `driverquery | findstr <keyword>`

#### Description:

- Filters driver list.
```cmd
driverquery | findstr wifi
```

#### Where & When Used:

- Locate specific drivers

---

## 🔌 Shutdown & Restart Commands

### 📌 `shutdown /f /r /fw /t 0`

#### Description:

- Force restart into firmware (UEFI/BIOS).
```cmd
shutdown /r /fw /f /t 0
```

#### Where & When Used:

- BIOS/UEFI access

### 📌 `shutdown /f /r /t 0`

#### Description:

- Immediate forced restart.
```cmd
shutdown /f /r /t 0
```

#### Where & When Used:

- System reboot

---
