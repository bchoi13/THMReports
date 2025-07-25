# TryHackMe - Windows Forensics 1

https://tryhackme.com/room/windowsforensics1

## 📘 Overview

**Room Name:** Windows Forensics 1  

**Difficulty:** Medium

**Objective:** This room showcases forensic analysis in Windows OS via Windows Registry.

**Date Completed:** [06/01/2025]

---

## 🎯 Target Information
| Detail        | Value              |
|---------------|--------------------|
| IP Address     | [N/A / No CTF]        |
| Operating System |  Windows   |
| Applications Discovered | [EZViewer, Autopsy,] |

---

## 🛠️ Tools Used
- Registry Editor - regedit.exe. Basic executable that opens up window of system's registry. 
- Registry Viewer - [User interface for viewing registry, though only allows access to one registry hive at a time.]
- Zimmerman's Registry Explorer - [Similar to the aforementioned Registry Viewer (AccessData), but able to load multiple hives at once. Can also import data from transaction logs. ]
- RegRipper - [Input registry hive, output data report.]

### Note:
| Item     | Definition    | Example |
|----------|---------------|---------|
| Hive | Group of keys, subkeys, and values containing set of supporting values loaded into memory when OS starts up; inside the registry. | HKEY_LOCAL_MACHINE\Security |
| Transaction Logs | Journal of changelog of the registry. | C:\Windows\System32\Config

---

