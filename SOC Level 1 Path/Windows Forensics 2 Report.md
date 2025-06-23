# TryHackMe - Windows Forensics 2 Walkthrough

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
MFTECmd.exe -f C:\Users\THM-4n6\Desktop\triage\C\$MFT -csv C:\Users\THM-4n6\Desktop

Parse data from different NTFS files. Outputs as a csv. Here we are able to view data points such as filename, created date, modified dates, access dates, and much more, all displayed in excel format. 
```

### 🔎 PECmd.exe
```bash

Findings:

PECmd.exe -d C:\Users\THM-4n6\Desktop\triage\C\Windows\prefetch -csv C:\Users\THM-4n6\Desktop

Prefetch parser used to output parsed file as 2 different csv's. Prefetch files contain information used to load a program quickly if used frequently. Inside the csv, we are able to locate data such as last time of execution and times executed for different files in our system.
```

### 🔎 WxTCmd.exe
```bash

Findings:

WxTCmd.exe -f C:\Users\THM-4n6\Desktop\triage\C\Users\THM-4n6\AppData\Local\ConnectedDevicesPlatform\L.THM-4n6\ActivitiesCache.db — csv C:\Users\THM-4n6\Desktop

Windows 10 timeline parser. Source of information for last executed processes.
```

### 🔎 JLECmd.exe

```bash

Findings:

JLECmd.exe -d C:\Users\THM-4n6\Desktop\triage\C\Users\THM-4n6\AppData\Roaming\Microsoft\Windows\Recent\AutomaticDestinations — csv C:\Users\THM-4n6\Desktop

Jumplists parser. Jumplists were introduced by Windows 10 as a way for users to directly access recently used files from their taskbar. 

```

### 🔎 LECmd.exe
```bash

Findings:

LECmd.exe -d C:\Users\THM-4n6\Desktop\triage\C\Users\THM-4n6\AppData\Roaming\Microsoft\Windows\Recent\ — csv C:\Users\THM-4n6\Desktop

Lnk Explorer. Used to parse shortcut files. Command outputs csv containing data viewed in an excel spreadsheet format. Can view data such as last open time, creation time, modified time. 
```


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




