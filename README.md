# 🛡️ Ransomware Analysis: `<RANSOMWARE>`

This repository contains a structured analysis of the `<RANSOMWARE>` ransomware sample, conducted to understand its behavior, encryption mechanisms, and impact on infected systems.

As a beginner in cybersecurity and malware analysis, this project was undertaken to gain **hands-on experience** in:

- Static and dynamic analysis  
- Reverse engineering  
- Behavioral analysis using sandboxes  
- Threat intelligence gathering and documentation

---

## 🎯 Objectives

- **Static Analysis**  
  Analyze the binary without execution to extract strings, imports, and other metadata.

- **Dynamic Analysis**  
  Execute the malware in a sandbox (Any.Run) to observe real-time behavior, file activity, and network connections.

- **Reverse Engineering**  
  Use Ghidra to reverse-engineer key functions, especially those related to encryption and ransom note creation.

- **Behavioral Analysis**  
  Document indicators of compromise (IoCs) and study system modifications during execution.

- **Threat Intelligence**  
  Summarize findings in a clear format to contribute to the infosec community.

---

## ⚙️ Tools & Environment

| Tool        | Purpose                      |
|-------------|------------------------------|
| Ghidra      | Static and reverse analysis  |
| Any.Run     | Dynamic behavior sandbox     |
| Strings     | String extraction            |
| PEStudio    | PE header and import review  |
| VirtualBox  | Isolated VM environment      |

- **Note**: All analysis was done in a controlled and isolated virtual environment to prevent any risk to the host system.

---

## 🔍 Analysis Summary

### Static Analysis
- Extracted PE headers, suspicious strings, and import table data.
- Identified common ransomware API calls such as:
  - `CryptEncrypt`
  - `CreateFile`
  - `WriteFile`
  - `GetSystemDirectory`

### Dynamic Analysis
- Observed encryption of files and ransom note deployment.
- Captured screenshots of behavior in Any.Run.
- Noted process tree, network traffic, and system modifications.

### Reverse Engineering
- Decompiled key functions in Ghidra.
- Located encryption routine and embedded ransom message.
- Discovered anti-analysis techniques used to avoid detection.

---

## 📌 Key Findings

- Encrypts files with a **custom file extension**.
- Drops and displays a **ransom note** demanding payment.
- Uses **anti-debugging and evasion tactics** to avoid analysis.
- Contacts external servers (C2 communication observed in some runs).

---

## 🗂️ Repository Structure

