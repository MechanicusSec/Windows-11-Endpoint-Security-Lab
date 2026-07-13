# Windows Security Command Notes

## Purpose

This file contains useful commands from the Windows 11 Endpoint Security Lab.

The goal is to collect the main PowerShell, Windows management and Git commands used during the lab into one readable reference.

These notes can be reused during endpoint security reviews, helpdesk troubleshooting, documentation work and junior sysadmin practice.

---

## Project setup commands

### mkdir

```powershell
mkdir docs, notes, results, screenshots, scripts
```

Purpose:

Creates the main project folders.

In this lab, the folders were used for documentation, notes, results, screenshots and optional scripts.

---

### New-Item

```powershell
New-Item README.md, logbook.md -ItemType File
```

Purpose:

Creates the starter `README.md` and `logbook.md` files.

`README.md` is the main project overview.

`logbook.md` is the chronological project journal.

---

### New-Item for .gitkeep files

```powershell
New-Item docs\.gitkeep, notes\.gitkeep, results\.gitkeep, screenshots\.gitkeep, scripts\.gitkeep -ItemType File
```

Purpose:

Creates `.gitkeep` placeholder files inside empty folders.

Git does not track empty folders by default, so `.gitkeep` files allow the folder structure to be included in the repository.

---

### tree /F

```powershell
tree /F
```

Purpose:

Shows the project folder structure and files.

This is useful for confirming that the expected folders and starter files were created.

---

## Windows Security baseline commands

### Get-MpComputerStatus

```powershell
Get-MpComputerStatus
```

Purpose:

Shows Microsoft Defender Antivirus status.

This command can show whether Defender components are enabled, such as antivirus, antispyware, behavior monitoring and real-time protection.

Useful fields may include:

```text
AMServiceEnabled
AntivirusEnabled
AntispywareEnabled
BehaviorMonitorEnabled
RealTimeProtectionEnabled
AntivirusSignatureLastUpdated
QuickScanAge
FullScanAge
```

This is useful for verifying Defender status from PowerShell after reviewing Windows Security in the GUI.

---

## Windows Firewall commands

### Get-NetFirewallProfile

```powershell
Get-NetFirewallProfile
```

Purpose:

Shows Windows Defender Firewall profile configuration.

The main profiles are:

```text
Domain
Private
Public
```

Useful fields may include:

```text
Name
Enabled
DefaultInboundAction
DefaultOutboundAction
NotifyOnListen
LogFileName
```

This command is useful for checking whether firewall profiles are enabled.

---

### Get-NetFirewallRule

```powershell
Get-NetFirewallRule | Select-Object -First 10
```

Purpose:

Lists Windows Defender Firewall rules.

`Get-NetFirewallRule` can return a very long list, so this lab used:

```powershell
Select-Object -First 10
```

to show only the first 10 rules.

The pipe symbol:

```powershell
|
```

sends the output from one command into another command.

This is useful for confirming that firewall rules exist without flooding the terminal.

---

## UAC and local administrator review commands

### Get-LocalUser

```powershell
Get-LocalUser
```

Purpose:

Lists local user accounts on the Windows machine.

Useful fields may include:

```text
Name
Enabled
Description
LastLogon
PasswordRequired
```

This is useful for reviewing which local accounts exist on an endpoint.

---

### Get-LocalGroupMember Administrators

```powershell
Get-LocalGroupMember Administrators
```

Purpose:

Lists members of the local Administrators group.

This is useful for checking which accounts have local administrator rights.

Local administrator membership should be reviewed carefully because admin accounts can make system-wide changes.

---

## BitLocker and device encryption commands

### manage-bde -status

```powershell
manage-bde -status
```

Purpose:

Shows BitLocker status for available volumes.

Useful fields may include:

```text
Conversion Status
Percentage Encrypted
Encryption Method
Protection Status
Lock Status
Key Protectors
```

This command may require PowerShell or Command Prompt to be opened as Administrator.

If access is denied, reopen PowerShell as Administrator and run it again.

---

### Get-BitLockerVolume

```powershell
Get-BitLockerVolume
```

Purpose:

Shows BitLocker volume status through PowerShell.

Useful fields may include:

```text
MountPoint
VolumeStatus
ProtectionStatus
EncryptionPercentage
EncryptionMethod
KeyProtector
```

This is useful for verifying encryption status from PowerShell.

In a virtual machine, BitLocker or Device encryption may be unavailable, disabled or limited depending on Windows edition and VM configuration.

---

## Apps and startup review commands

### Installed apps from registry

```powershell
Get-ItemProperty HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\* | Select-Object DisplayName, DisplayVersion, Publisher
```

Purpose:

Lists installed application entries from the Windows Registry.

The registry path:

```powershell
HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\*
```

contains many installed-program entries.

The selected fields are:

```text
DisplayName
DisplayVersion
Publisher
```

This is useful for collecting a basic software inventory from PowerShell.

---

### Startup commands

```powershell
Get-CimInstance Win32_StartupCommand
```

Purpose:

Lists startup commands configured on the Windows machine.

Useful fields may include:

```text
Name
Command
Location
User
```

This is useful for reviewing programs or commands that may start automatically when a user signs in.

---

## Security Event Viewer commands

### Get-WinEvent for Security log

```powershell
Get-WinEvent -LogName Security -MaxEvents 10
```

Purpose:

Reads the 10 newest events from the Windows Security log.

`Get-WinEvent` reads Windows event logs.

`-LogName Security` selects the Security log.

`-MaxEvents 10` limits the output to the 10 newest events.

This is useful for verifying Security log access from PowerShell.

Security log access may require administrator permissions.

---

## Local folder permissions commands

### Create test folder

```powershell
mkdir C:\Temp\SecurityLabTest
```

Purpose:

Creates a safe temporary test folder for permission review.

The lab used a test folder so no real user data or production folders were modified.

---

### Test folder existence

```powershell
Test-Path C:\Temp\SecurityLabTest
```

Purpose:

Checks whether the test folder exists.

Expected result after creation:

```text
True
```

Expected result after cleanup:

```text
False
```

---

### icacls

```powershell
icacls C:\Temp\SecurityLabTest
```

Purpose:

Displays NTFS permissions for the folder.

Common permission codes include:

```text
F  = Full control
M  = Modify
RX = Read and execute
R  = Read
W  = Write
I  = Inherited permission
OI = Object inherit
CI = Container inherit
```

This is useful for checking folder permissions from the command line.

---

### Remove-Item

```powershell
Remove-Item C:\Temp\SecurityLabTest -Recurse -Force
```

Purpose:

Deletes the temporary test folder.

`-Recurse` deletes everything inside the folder.

`-Force` removes items without extra prompts where possible.

This was used to clean up the lab folder after the permissions review.

---

## Git commands

### git status

```powershell
git status
```

Purpose:

Shows the current Git working tree state.

This tells you which files are changed, untracked, staged or ready to commit.

---

### git add

```powershell
git add README.md logbook.md
```

Purpose:

Stages files for the next commit.

Staging means telling Git which files should be included in the next saved checkpoint.

---

### git commit

```powershell
git commit -m "Commit message here"
```

Purpose:

Creates a local Git checkpoint.

The message should describe what changed.

Example:

```powershell
git commit -m "Add local folder permissions review"
```

---

### git push

```powershell
git push
```

Purpose:

Uploads local commits to GitHub.

This makes the latest project version available in the remote repository.

---

## Notes

These commands were used in a safe Windows 11 virtual machine lab.

The commands support common endpoint security review tasks such as:

* Checking Microsoft Defender status.
* Reviewing firewall profiles and rules.
* Checking local users and administrator membership.
* Reviewing BitLocker or device encryption status.
* Reviewing installed applications and startup commands.
* Reading Security log events.
* Checking NTFS folder permissions.
* Documenting and publishing work with Git.

Commands should be tested in a lab environment before being used on real systems.

No real user data, production systems or private company devices were used in this project.
