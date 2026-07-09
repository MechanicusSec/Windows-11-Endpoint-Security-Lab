# Windows 11 Endpoint Security Lab

## Overview

Windows 11 Endpoint Security Lab is a practical IT support and junior sysadmin portfolio project focused on reviewing and documenting the basic security posture of a Windows 11 endpoint.

The lab covers Windows Security, Windows Defender Firewall, User Account Control, local users and groups, BitLocker or device encryption review, installed apps, startup apps, security event logs, folder permissions, command notes and final reporting.

This project uses a safe local lab environment only.

No real user data, production systems, passwords, private files or company devices are used.

## Scenario

A Windows 11 client needs a basic endpoint security review.

The goal of this lab is to act as an IT support technician or junior sysadmin and review common endpoint security areas using Windows GUI tools, PowerShell and structured documentation.

The project demonstrates how a technician can inspect security settings, verify important controls, document findings and produce a final endpoint security report.

## Lab environment

| Component | Description |
| --- | --- |
| Host system | Windows workstation used for documentation, screenshots, Git and GitHub workflow |
| Lab system | Windows 11 virtual machine |
| Virtualization | VMware-based Windows 11 VM |
| Lab user | Local lab account |
| Documentation tools | VS Code, Markdown, Git and GitHub |
| Evidence | Screenshots, results notes and final report |

## Planned parts

| Part | Topic | Status |
| --- | --- | --- |
| Part 1 | Project setup | Complete |
| Part 2 | Windows Security baseline | Complete |
| Part 3 | Windows Firewall review | Complete |
| Part 4 | UAC and admin rights review | Planned |
| Part 5 | BitLocker or device encryption review | Planned |
| Part 6 | Apps and startup review | Planned |
| Part 7 | Security Event Viewer review | Planned |
| Part 8 | Local folder permissions review | Planned |
| Part 9 | Security command notes | Planned |
| Part 10 | Final endpoint security report | Planned |

## Project structure

```text
Windows-11-Endpoint-Security-Lab/
├── docs/
├── notes/
├── results/
├── screenshots/
├── scripts/
├── logbook.md
└── README.md
```

## Current evidence

| Screenshot | Description |
| --- | --- |
| screenshots/screenshot-01-project-structure.png | Shows the initial project folder structure. |
| screenshots/screenshot-02a-windows-security-home.png | Shows the Windows Security home dashboard. |
| screenshots/screenshot-02b-virus-threat-protection.png | Shows Virus & threat protection. |
| screenshots/screenshot-02c-account-protection.png | Shows Account protection. |
| screenshots/screenshot-02d-firewall-network-protection.png | Shows Firewall & network protection during the baseline review. |
| screenshots/screenshot-02e-app-browser-control.png | Shows App & browser control. |
| screenshots/screenshot-02f-device-security.png | Shows Device security. |
| screenshots/screenshot-02g-defender-powershell-status.png | Shows Microsoft Defender status checked with PowerShell. |
| screenshots/screenshot-03a-firewall-network-protection.png | Shows Firewall & network protection during the firewall review. |
| screenshots/screenshot-03b-firewall-active-profile.png | Shows the active firewall network profile. |
| screenshots/screenshot-03c-firewall-allowed-apps.png | Shows the allowed apps through firewall view. |
| screenshots/screenshot-03d-firewall-powershell-profiles.png | Shows firewall profile status checked with PowerShell. |
| screenshots/screenshot-03e-firewall-powershell-rules.png | Shows a sample of firewall rules listed with PowerShell. |

## Results and documentation

| File | Description |
| --- | --- |
| README.md | Main project overview and progress tracker. |
| logbook.md | Chronological project logbook. |
| results/windows-security-baseline-results.txt | Written summary of the Windows Security baseline review. |
| results/windows-firewall-review-results.txt | Written summary of the Windows Firewall review. |

## Skills demonstrated

This lab demonstrates:

* Windows 11 endpoint security review.
* Windows Security navigation.
* Microsoft Defender baseline review.
* Windows Firewall review.
* Firewall profile inspection.
* Allowed apps through firewall review.
* PowerShell firewall verification.
* PowerShell security status verification.
* User Account Control review.
* Local users and groups inspection.
* Local administrator membership review.
* BitLocker or device encryption status review.
* Installed apps review.
* Startup apps review.
* Security event log review.
* NTFS folder permission review.
* Screenshot evidence collection.
* Technical documentation.
* Git and GitHub workflow.

## Tools and commands used

| Tool or command | Purpose |
| --- | --- |
| File Explorer | Used to create and review the project folder. |
| VS Code | Used to edit Markdown documentation and manage project files. |
| PowerShell terminal | Used to create folders, create files and run Git commands. |
| Git | Used for local version control. |
| GitHub | Used to publish the project as portfolio evidence. |
| Windows Settings | Used to open Windows Security and review endpoint settings. |
| Windows Security | Used to review built-in Windows endpoint security areas. |
| Virus & threat protection | Used to review Microsoft Defender Antivirus baseline status. |
| Account protection | Used to review account-related security areas. |
| Firewall & network protection | Used to review Windows Defender Firewall status. |
| App & browser control | Used to review reputation-based protection and exploit protection areas. |
| Device security | Used to review device security and hardware-backed security areas. |
| Allowed apps through firewall | Used to review which apps are allowed through Windows Defender Firewall. |
| `mkdir docs, notes, results, screenshots, scripts` | Creates the main project folders. |
| `New-Item README.md, logbook.md -ItemType File` | Creates the starter README and logbook files. |
| `New-Item docs\.gitkeep, notes\.gitkeep, results\.gitkeep, screenshots\.gitkeep, scripts\.gitkeep -ItemType File` | Creates placeholder files so Git can track empty folders. |
| `tree /F` | Shows the project folder structure and files. |
| `git init` | Initializes the local Git repository. |
| `git add` | Stages files for commit. |
| `git commit` | Creates a local Git checkpoint. |
| `git remote add origin` | Connects the local repository to GitHub. |
| `git branch -M main` | Renames the current branch to main. |
| `git push` | Uploads local commits to GitHub. |
| `git status` | Shows the current Git working tree state. |
| `Get-MpComputerStatus` | Shows Microsoft Defender Antivirus status and protection state. |
| `Get-NetFirewallProfile` | Shows Windows Defender Firewall profile configuration for Domain, Private and Public profiles. |
| `Get-NetFirewallRule \| Select-Object -First 10` | Lists a small sample of Windows Defender Firewall rules. |

## Key endpoint security lessons

### Windows Security baseline

Part 2 demonstrated how to open and review the main Windows Security dashboard.

The lab reviewed Virus & threat protection, Account protection, Firewall & network protection, App & browser control and Device security. PowerShell was then used to verify Microsoft Defender status with `Get-MpComputerStatus`.

### Windows Firewall review

Part 3 demonstrated how to review Windows Defender Firewall through the GUI and PowerShell.

The lab reviewed the active network profile, allowed apps through firewall, firewall profile status and a sample of firewall rules. This showed how a technician can confirm that firewall protections are visible and configurable through normal Windows tools.

## Project evidence policy

Screenshots in this project should focus on the actual Windows 11 endpoint security work and project files.

GitHub repository pages and push screens are not required as screenshot evidence unless specifically needed later. GitHub activity is documented through Git commits and the project documentation instead.

## Privacy notes

This project does not include real user data, private passwords, license keys, personal Microsoft account information or production company data.

Local user paths should be documented using:

```text
C:\Users\*****
```

instead of the real Windows username.

Screenshots should avoid exposing personal account names, private host paths, real passwords, license keys, private files or unrelated personal information.
