# TryHackMe - Windows Forensics 1 Walkthrough [In Progress]

## 📘 Overview
**Room Name:** Windows Forensics 1  
**Difficulty:** Medium
**Objective:** This room showcases forensic analysis in Windows OS via Windows Registry.
**Date Completed:** [MM/DD/YYYY]

---

## 🎯 Target Information
| Detail        | Value              |
|---------------|--------------------|
| IP Address     | [Target IP]        |
| Operating System | [Windows/Linux]   |
| Services Discovered | [e.g. HTTP, SSH, SMB] |

---

## 🛠️ Tools Used
- Registry Editor - regedit.exe. Basic executable that opens up window of system's registry. 
- Registry Viewer - [Purpose]
- Zimmerman's Registry Explorer - [Purpose]
- RegRipper - [Purpose]

---

## 🔍 Enumeration

### 🔎 Nmap Scan
```bash
nmap -sC -sV -oN nmap_initial [IP]

