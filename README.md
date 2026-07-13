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
| Part 4 | UAC and admin rights review | Complete |
| Part 5 | BitLocker or device encryption review | Complete |
| Part 6 | Apps and startup review | Complete |
| Part 7 | Security Event Viewer review | Complete |
| Part 8 | Local folder permissions review | Complete |
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
| screenshots/screenshot-04a-uac-settings.png | Shows User Account Control settings. |
| screenshots/screenshot-04b-computer-management-local-users.png | Shows local users in Computer Management. |
| screenshots/screenshot-04c-local-user-properties.png | Shows local user account properties. |
| screenshots/screenshot-04d-administrators-group-members.png | Shows local Administrators group members. |
| screenshots/screenshot-04e-powershell-local-users.png | Shows local users listed with PowerShell. |
| screenshots/screenshot-04f-powershell-administrators-group.png | Shows local Administrators group members listed with PowerShell. |
| screenshots/screenshot-05a-device-encryption-settings.png | Shows Device encryption settings or search result. |
| screenshots/screenshot-05b-bitlocker-control-panel.png | Shows BitLocker Drive Encryption in Control Panel. |
| screenshots/screenshot-05d-manage-bde-status-admin.png | Shows BitLocker status checked with manage-bde from an elevated PowerShell session. |
| screenshots/screenshot-05e-powershell-bitlocker-volume.png | Shows BitLocker volume status checked with PowerShell. |
| screenshots/screenshot-06a-installed-apps-settings.png | Shows Installed apps in Windows Settings. |
| screenshots/screenshot-06b-startup-apps-settings.png | Shows Startup apps in Windows Settings. |
| screenshots/screenshot-06c-task-manager-startup-apps.png | Shows Startup apps in Task Manager. |
| screenshots/screenshot-06d-powershell-installed-apps.png | Shows installed applications listed with PowerShell. |
| screenshots/screenshot-06e-powershell-startup-commands.png | Shows startup commands listed with PowerShell. |
| screenshots/screenshot-07a-event-viewer-security-log.png | Shows the Security log opened in Event Viewer. |
| screenshots/screenshot-07b-security-log-recent-events.png | Shows recent Security log events. |
| screenshots/screenshot-07c-security-log-filter-current-log.png | Shows the Filter Current Log window for Security event filtering. |
| screenshots/screenshot-07d-security-log-filtered-logon-events.png | Shows filtered logon-related Security events. |
| screenshots/screenshot-07e-security-event-details.png | Shows details for Security Event ID 4672. |
| screenshots/screenshot-07f-powershell-security-log.png | Shows Security log access checked with PowerShell. |
| screenshots/screenshot-08a-security-test-folder-created.png | Shows the temporary security test folder created and confirmed with PowerShell. |
| screenshots/screenshot-08b-folder-security-tab.png | Shows the folder Security tab and NTFS permissions view. |
| screenshots/screenshot-08c-folder-advanced-security-settings.png | Shows Advanced security settings for the test folder. |
| screenshots/screenshot-08d-powershell-icacls-permissions.png | Shows NTFS permissions checked with icacls. |
| screenshots/screenshot-08e-folder-cleanup-confirmed.png | Shows the test folder cleanup confirmed with Test-Path. |

## Results and documentation

| File | Description |
| --- | --- |
| README.md | Main project overview and progress tracker. |
| logbook.md | Chronological project logbook. |
| results/windows-security-baseline-results.txt | Written summary of the Windows Security baseline review. |
| results/windows-firewall-review-results.txt | Written summary of the Windows Firewall review. |
| results/uac-admin-rights-review-results.txt | Written summary of the UAC and admin rights review. |
| results/bitlocker-device-encryption-review-results.txt | Written summary of the BitLocker or device encryption review. |
| results/apps-startup-review-results.txt | Written summary of the apps and startup review. |
| results/security-event-viewer-review-results.txt | Written summary of the Security Event Viewer review. |
| results/local-folder-permissions-review-results.txt | Written summary of the local folder permissions review. |

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
* Local account property review.
* Computer Management navigation.
* PowerShell local account verification.
* BitLocker or device encryption status review.
* BitLocker Control Panel review.
* Device encryption availability review.
* Disk encryption command-line verification.
* Installed apps review.
* Installed applications inventory review.
* Startup apps review.
* Startup apps review through Settings and Task Manager.
* Security event log review.
* Event Viewer Security log review.
* Security event filtering.
* PowerShell Security log verification.
* NTFS folder permission review.
* Folder Security tab review.
* Advanced NTFS permission review.
* PowerShell folder permission verification.
* Safe test folder creation and cleanup.
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
| User Account Control settings | Used to review the UAC notification level. |
| Computer Management | Used to review local users and local groups. |
| Local Users and Groups | Used to inspect local accounts and group membership. |
| Administrators group | Used to identify accounts with local administrator rights. |
| Device encryption settings | Used to review whether Windows Device encryption is available. |
| Control Panel | Used to access the classic BitLocker Drive Encryption interface. |
| BitLocker Drive Encryption | Used to review drive encryption status and BitLocker management options. |
| Elevated PowerShell | Used to run BitLocker commands that require administrative rights. |
| Installed apps settings | Used to review installed applications in Windows Settings. |
| Startup apps settings | Used to review apps configured to start automatically when the user signs in. |
| Task Manager | Used to review startup apps and startup impact. |
| Event Viewer | Used to review Windows event logs. |
| Security log | Used to review Windows audit and logon-related events. |
| Filter Current Log | Used to filter Security log events by specific event IDs. |
| Folder Properties | Used to review folder information and Security tab permissions. |
| Security tab | Used to review NTFS permissions for the test folder. |
| Advanced security settings | Used to review inherited permissions, ownership and detailed permission entries. |
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
| `Get-LocalUser` | Lists local user accounts on the Windows machine. |
| `Get-LocalGroupMember Administrators` | Lists members of the local Administrators group. |
| `manage-bde -status` | Shows BitLocker status for available volumes. |
| `Get-BitLockerVolume` | Shows BitLocker volume status through PowerShell. |
| `Get-ItemProperty HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\* \| Select-Object DisplayName, DisplayVersion, Publisher` | Lists installed application entries from the Windows Registry and shows selected application details. |
| `Get-CimInstance Win32_StartupCommand` | Lists startup commands configured on the Windows machine. |
| `Get-WinEvent -LogName Security -MaxEvents 10` | Reads the 10 newest events from the Windows Security log. |
| `mkdir C:\Temp\SecurityLabTest` | Creates a safe temporary folder for permissions review. |
| `Test-Path C:\Temp\SecurityLabTest` | Checks whether the temporary test folder exists. |
| `icacls C:\Temp\SecurityLabTest` | Displays NTFS permissions for the temporary test folder. |
| `Remove-Item C:\Temp\SecurityLabTest -Recurse -Force` | Deletes the temporary test folder and its contents. |

## Key endpoint security lessons

### Windows Security baseline

Part 2 demonstrated how to open and review the main Windows Security dashboard.

The lab reviewed Virus & threat protection, Account protection, Firewall & network protection, App & browser control and Device security. PowerShell was then used to verify Microsoft Defender status with `Get-MpComputerStatus`.

### Windows Firewall review

Part 3 demonstrated how to review Windows Defender Firewall through the GUI and PowerShell.

The lab reviewed the active network profile, allowed apps through firewall, firewall profile status and a sample of firewall rules. This showed how a technician can confirm that firewall protections are visible and configurable through normal Windows tools.

### UAC and admin rights review

Part 4 demonstrated how to review User Account Control settings and local administrator membership.

The lab reviewed UAC settings, local users, local user account properties, the Administrators group and PowerShell verification of local accounts and administrator membership. This showed how a technician can identify which accounts exist locally and which accounts have elevated privileges.

### BitLocker or device encryption review

Part 5 demonstrated how to review Windows drive encryption status.

The lab reviewed Device encryption settings, BitLocker Drive Encryption in Control Panel, `manage-bde -status` from an elevated PowerShell session and `Get-BitLockerVolume`. This showed how a technician can verify whether drive encryption is available, enabled, disabled or limited in a Windows 11 VM.

### Apps and startup review

Part 6 demonstrated how to review installed applications and startup items.

The lab reviewed Installed apps in Windows Settings, Startup apps in Windows Settings, Startup apps in Task Manager, installed application entries through PowerShell and startup commands through PowerShell. This showed how a technician can identify installed software and auto-start entries that may affect endpoint performance or security.

### Security Event Viewer review

Part 7 demonstrated how to inspect Windows Security logs.

The lab reviewed the Security log in Event Viewer, filtered logon-related events, opened Event ID 4672 for detailed review and verified Security log access with `Get-WinEvent`. This showed how a technician can review audit events and understand that Security log entries should be interpreted with context rather than treated as automatic proof of an active issue.

### Local folder permissions review

Part 8 demonstrated how to inspect NTFS folder permissions.

The lab created a safe temporary test folder, reviewed the folder Security tab, opened Advanced security settings, verified permissions with `icacls` and removed the test folder afterward. This showed how a technician can inspect local file permissions without touching real user data or production folders.

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
