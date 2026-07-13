# Windows 11 Endpoint Security Lab — Final Report

## Overview

This report summarizes the Windows 11 Endpoint Security Lab.

The purpose of this project was to perform a basic endpoint security review of a Windows 11 virtual machine using GUI tools, PowerShell commands, screenshots, written results and structured documentation.

The lab was completed in a safe local environment. No real user data, production systems, private files, passwords or company devices were used.

## Scenario

A Windows 11 client needed a basic endpoint security review.

The role in this scenario was an IT support technician or junior sysadmin reviewing common endpoint security areas and documenting the findings in a clear and repeatable way.

The review focused on built-in Windows security controls, local configuration, security logs, software inventory, startup behavior and local folder permissions.

## Lab environment

| Component | Description |
| --- | --- |
| Host system | Windows workstation used for documentation, screenshots, Git and GitHub workflow |
| Lab system | Windows 11 virtual machine |
| Virtualization | VMware-based Windows 11 VM |
| Lab user | Local lab account |
| Documentation tools | VS Code, Markdown, Git and GitHub |
| Evidence | Screenshots, results notes, command notes and final report |

## Project parts completed

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
| Part 9 | Security command notes | Complete |
| Part 10 | Final endpoint security report | Complete |

## Areas reviewed

### Windows Security baseline

The Windows Security dashboard was reviewed to inspect the main built-in endpoint security areas.

Reviewed areas included:

* Virus & threat protection.
* Account protection.
* Firewall & network protection.
* App & browser control.
* Device security.

PowerShell was used to verify Microsoft Defender status with:

```powershell
Get-MpComputerStatus
```

This confirmed how Microsoft Defender status can be checked from the command line after reviewing the graphical interface.

### Windows Firewall

Windows Defender Firewall was reviewed through the Windows Security GUI and PowerShell.

The lab reviewed:

* Firewall & network protection.
* Active network profile.
* Domain, Private and Public firewall profiles.
* Allowed apps through firewall.
* Firewall profile status.
* A sample of firewall rules.

PowerShell commands used:

```powershell
Get-NetFirewallProfile
Get-NetFirewallRule | Select-Object -First 10
```

This demonstrated how firewall status can be reviewed through both GUI tools and command-line verification.

### User Account Control and local administrator rights

User Account Control settings and local administrator membership were reviewed.

The lab reviewed:

* UAC notification level.
* Local users in Computer Management.
* Local user properties.
* Local Administrators group membership.
* PowerShell verification of local users and administrator group members.

PowerShell commands used:

```powershell
Get-LocalUser
Get-LocalGroupMember Administrators
```

This demonstrated how a technician can inspect local accounts and identify which accounts have local administrator rights.

### BitLocker or Device encryption

BitLocker and Device encryption availability were reviewed.

The lab reviewed:

* Device encryption settings.
* BitLocker Drive Encryption in Control Panel.
* BitLocker status through `manage-bde`.
* BitLocker volume status through PowerShell.

Commands used:

```powershell
manage-bde -status
Get-BitLockerVolume
```

The lab also showed that some BitLocker commands may require administrative rights.

In a virtual machine, BitLocker or Device encryption may be unavailable, disabled or limited depending on Windows edition and virtual hardware configuration.

### Installed apps and startup apps

Installed applications and startup apps were reviewed as part of endpoint hygiene.

The lab reviewed:

* Installed apps in Windows Settings.
* Startup apps in Windows Settings.
* Startup apps in Task Manager.
* Installed application entries through PowerShell.
* Startup commands through PowerShell.

PowerShell commands used:

```powershell
Get-ItemProperty HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\* | Select-Object DisplayName, DisplayVersion, Publisher
Get-CimInstance Win32_StartupCommand
```

This demonstrated how a technician can review installed software and automatic startup entries.

### Security Event Viewer

The Windows Security log was reviewed using Event Viewer and PowerShell.

The lab reviewed:

* Event Viewer.
* Windows Logs.
* Security log.
* Recent Security events.
* Filtered logon-related events.
* Event ID 4672 details.
* Security log access through PowerShell.

PowerShell command used:

```powershell
Get-WinEvent -LogName Security -MaxEvents 10
```

Event IDs reviewed:

| Event ID | Meaning |
| --- | --- |
| 4624 | Successful logon |
| 4625 | Failed logon |
| 4634 | Logoff |
| 4672 | Special privileges assigned to a new logon |

The lab demonstrated how Security log entries can be reviewed and interpreted with context.

### Local folder permissions

NTFS folder permissions were reviewed on a safe temporary test folder.

The lab reviewed:

* Test folder creation.
* Folder Properties.
* Security tab.
* Advanced security settings.
* NTFS permissions through `icacls`.
* Cleanup of the test folder.

Commands used:

```powershell
mkdir C:\Temp\SecurityLabTest
Test-Path C:\Temp\SecurityLabTest
icacls C:\Temp\SecurityLabTest
Remove-Item C:\Temp\SecurityLabTest -Recurse -Force
Test-Path C:\Temp\SecurityLabTest
```

The test folder was removed after the review. No real user data or production folders were modified.

### Security command notes

A reusable command reference was created:

```text
notes/windows-security-command-notes.md
```

The notes file collects the main commands used during the lab and explains their purpose.

This supports review, reuse and interview preparation.

## Evidence collected

Evidence was collected through:

* Screenshots.
* Results files.
* Logbook entries.
* README updates.
* Command notes.
* Final report.
* Git commits.

## Results files created

| File | Purpose |
| --- | --- |
| results/windows-security-baseline-results.txt | Summary of the Windows Security baseline review. |
| results/windows-firewall-review-results.txt | Summary of the Windows Firewall review. |
| results/uac-admin-rights-review-results.txt | Summary of the UAC and admin rights review. |
| results/bitlocker-device-encryption-review-results.txt | Summary of the BitLocker or device encryption review. |
| results/apps-startup-review-results.txt | Summary of the apps and startup review. |
| results/security-event-viewer-review-results.txt | Summary of the Security Event Viewer review. |
| results/local-folder-permissions-review-results.txt | Summary of the local folder permissions review. |

## Skills demonstrated

This lab demonstrates:

* Windows 11 endpoint security review.
* Windows Security navigation.
* Microsoft Defender baseline verification.
* Windows Defender Firewall review.
* Firewall profile inspection.
* Allowed apps through firewall review.
* User Account Control review.
* Local users and groups inspection.
* Local administrator membership review.
* BitLocker and Device encryption status review.
* Installed applications review.
* Startup apps review.
* Security Event Viewer review.
* Security event filtering.
* PowerShell Security log verification.
* NTFS folder permission review.
* PowerShell command usage.
* GUI-first troubleshooting and verification.
* Technical documentation.
* Screenshot evidence collection.
* Git and GitHub workflow.

## Limitations

This lab was performed in a local Windows 11 virtual machine.

Some security features may behave differently in a VM compared to physical hardware. This can affect areas such as Device encryption, BitLocker, Secure Boot, TPM-related features and hardware-backed security options.

The lab did not include real production policies, enterprise endpoint management, Microsoft Intune, Microsoft Defender for Endpoint, Active Directory domain policies or centralized logging.

The purpose of the lab was not to harden a production device, but to practice endpoint security review and documentation in a safe learning environment.

## Privacy and safety

No real user data, production files, company systems, private passwords, license keys or personal Microsoft account data were used.

A temporary folder was created for the NTFS permissions review and removed after the test.

Local user paths should be documented using:

```text
C:\Users\*****
```

instead of the real Windows username.

Screenshots should avoid exposing personal account names, private files, private host paths, license keys, real passwords or unrelated personal information.

## Conclusion

The Windows 11 Endpoint Security Lab was completed successfully.

The project demonstrated how to perform and document a basic endpoint security review using built-in Windows tools, PowerShell, screenshots, results files and structured Markdown documentation.

The lab covered common review areas that are relevant for IT support, desktop support and junior sysadmin work, including Windows Security, Defender Firewall, local accounts, administrator rights, drive encryption, installed apps, startup items, Security logs and NTFS folder permissions.

The final project provides portfolio evidence of practical Windows 11 endpoint security review skills, documentation discipline and command-line verification.
