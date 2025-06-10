# TryHackMe - Windows Forensics 2 Walkthrough [In Progress]

## 📘 Overview
**Room Name:** Windows Forensics 2
**Difficulty:** Medium  
**Objective:** Learn about common Windows file systems and forensic artifacts in the file systems. Identify locations and artifacts 
to prove evidence of execution, file/folder usage or knowledge, and external device usage.  
**Date Completed:** [06/06/2025]

---

## 🎯 Target Information
| Detail        | Value              |
|---------------|--------------------|
| IP Address     | [N/A / No CTF]        |
| Operating System | Windows  |
| Applications Discovered | [Eric Zimmerman's Tools] |

---

## 🛠️ Tools Used
- EZViewer - Eric Zimmerman's dependancy viewer tool. Used to view csv files created in this room.
- Autopsy - Open source digital forensics platform. The purpose of this tool for this lab specifically is for the recovery of deleted files.

---

## 🔍 Enumeration

### 🔎 MFTECmd.exe
```bash

Findings:
```

### PECmd.exe

### LECmd.exe


Notes...

📂 Other Enumeration
Used EZViewer to comprehensively view csv data files created from executing the above processes.

Found important data objects listed in excel format. 

💥 Exploitation

N/A

🧰 Vulnerability Identified

N/A

CVE ID (if applicable): N/A

⚙️ Exploitation Steps

N/A

# Commands used
*See above enumeration

🚩 Post-Exploitation

N/A

🧍 Privilege Escalation

N/A


📜 Flags Captured

N/A


🧠 Lessons Learned
Key takeaways: THe Windows registry contains a plethora of important data that can be utilized for information gathering. 
This room presents us the way to parse the data of various different log files as well as convert the data into readable csv format.
The skills learned in this lab can be used during security analysis; for instance, discovering when a file was modified or first accessed
can be vital information for maintaining integrity. 

New tools or techniques learned: Eric ZImmerman's Tools. 

Any troubleshooting insights:



