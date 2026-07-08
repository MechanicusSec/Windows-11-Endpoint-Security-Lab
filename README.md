# Windows 11 Endpoint Security Lab

## Overview

Windows 11 Endpoint Security Lab is a practical IT support and junior sysadmin portfolio project focused on reviewing and documenting the basic security posture of a Windows 11 endpoint.

The lab covers Windows Security, Microsoft Defender, Windows Firewall, User Account Control, local users and groups, BitLocker or device encryption review, installed apps, startup apps, security event logs, folder permissions and final reporting.

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
| Part 2 | Windows Security baseline | Planned |
| Part 3 | Microsoft Defender review | Planned |
| Part 4 | Windows Firewall review | Planned |
| Part 5 | UAC and admin rights review | Planned |
| Part 6 | BitLocker or device encryption review | Planned |
| Part 7 | Apps and startup review | Planned |
| Part 8 | Security Event Viewer review | Planned |
| Part 9 | Local folder permissions review | Planned |
| Part 10 | Security command notes | Planned |
| Part 11 | Final endpoint security report | Planned |

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

## Results and documentation

| File | Description |
| --- | --- |
| README.md | Main project overview and progress tracker. |
| logbook.md | Chronological project logbook. |

## Skills demonstrated

This lab will demonstrate:

* Windows 11 endpoint security review.
* Windows Security navigation.
* Microsoft Defender review.
* Windows Firewall review.
* User Account Control review.
* Local users and groups inspection.
* Local administrator membership review.
* BitLocker or device encryption status review.
* Installed apps review.
* Startup apps review.
* Security event log review.
* NTFS folder permission review.
* PowerShell verification.
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
