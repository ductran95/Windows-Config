# Windows 10 installation for Lenovo Legion 5

# Disk partitions
* Disk 1: 238GB
  * Windows: 175GB
  * Works: 63GB
* Disk 2: 476GB
  * Arch-linux: 75GB
  * Entertainment: 400GB

# Create Installation USB
*  en_windows_10_business_editions_version_20h2_updated_jan_2021_x64_dvd_533a330d.iso
*  Rufus: GPT-UEFI-NTFS

# Install Windows
*  F1 + F2 => USB
*  Language: English, Format: English, Keyboard: US
*  Skip enter key
*  Custom: Install windows only
*  Delete partitions, recreate linux install partition
*  Username: DucTran
*  Online speech: Off, Diagnosis: Off, Tailored: Off

# Config UAC
*  Open Control Panel
*  View: Large Icons
*  User Accounts => Change User Accounts Control Setting
    *  Never Notify

# Config File Explorer setting
*  Open File Explorer
*  File => Change folder and search options => View
    *  Show hidden file, folder and drive
    *  Untick Hide empty drive
    *  Untick Hide extension
    *  Untick Hide folder merge conflict

# Config Power Option
*  Open Control Panel => Power Options
*  Choose what closing the lid
    *  power: sleep
    *  sleep: sleep
    *  close lid: Do nothing
*  Balaced => Change plan setting
    *  Turn off: 30 min
    *  Sleep: never
*  Change advanced setting
    *  Turn off hard disk: 0
    *  Wireless Adapter Setting: Medium power save, Maximun performance
    *  USB setting: Disabled
    *  PCI Express: Off
    *  Processor power => Minimum process state: 5%
    *  Processor power => System colling: Passive, Active
    *  Processor power => Maximum process state: 100%
    *  Multimedia => Sharing media: Allow sleep, Prevent sleep
    *  Multimedia => Video Playback: power-saving, performance
    *  Multimedia => Play video: balanced, video quality
    *  Battery => Critical battery notify: On
    *  Battery => Critical battery action: Shutdown
    *  Battery => Low battery level: 10%
    *  Battery => Critical battery level: 5%
    *  Battery => Low battery notify: On
    *  Battery => Low battery action: Nothing
    *  Battery => Reserved battery level: 7%

# Config Sync
*  Win+R: gpedit.msc
*  Computer Configuration => Admin Template => Windows Components => Sync your setting
*  Enabled all options

# Delete Windows SR
*  Open Control Panel => System => Advanced system settings => System Protection
*  Configure => Delete

# Config Service
*  Win+R: services.msc
*  Disable:
    *  Microsoft Software Shadow Copy
    *  Optimize drive
    *  Sysmain
    *  Volumn Shadow Copy

# Config Task Schedule
*  Win+R: taskschd.msc
*  Microsoft => Windows
*  Disable:
    *  Application Experience
    *  Application Data
    *  CloudExperienceHost
    *  Customer Experience Improvement Program
    *  Defrag
    *  DiskCleanup
    *  SystemRestore

# Config Display Scale
*  Open Settings => System
*  Scale and layout: 100%

# Turn off Hibernate file
*  Open cmd as admin
```bash
powercfg -h off
```

# Config Page file
*  Open Control Panel => System => Advanced system settings => Performance => Setting
*  Advanced => Virtual memery => Change
    *  Automatical manage: untick
    *  C: Custom size: 8192, 8192
*  Set => OK
*  Restart

# Install Drivers
* Update MS Store
* MS Store => Lenovo vantage
* Update driver

# Update windows
*  Clear temp files: %UserProfile%/AppData/Local/Temp
*  Start Task Manager
*  Connect wifi
*  Open Settings => Update & Security
*  Advanced Options => Receive updates for other Microsoft product: On
*  Delivery Optimization: Off
*  Check for update
*  Install Samsung Magician
*  Restart

# Active Window
*  Enter key: XGVPP-NMH47-7TTHJ-W3FW7-8HV2C
*  Customize Setting
    *  System Sound
    *  System Notification
    *  Time and Language
    *  Personalization
    *  Privacy

# Install Office 2019
*  en_office_professional_plus_2019_x86_x64_dvd_7ea28c99 => setup64
*  setuplanguagepack.x64.zh-cn_.exe
*  setuplanguagepack.x64.vi-vn_.exe
*  Active

# Install SQL Server 2019
*  en_sql_server_2019_enterprise_x64_dvd_46f0ba38.iso
*  Setting SQL service => Manual

# Install IIS, .Net Framework 3.5
*  Turn on feature
*  Add .Net Framework 3.5, IIS
*  Remove IE11

# Install Visual Studio
*  vs_Enterprise.exe

# Install Chocolatey
*  Open powershell as admin
* Run Get-ExecutionPolicy. If it returns Restricted, then run:
```bash
Set-ExecutionPolicy AllSigned
or
Set-ExecutionPolicy Bypass -Scope Process
```
* Run
```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

# Install Chocolatey GUI
* choco install chocolateygui

# Install SDK & Development Environment
* choco install sql-server-management-studio
* choco install postgresql
* choco install git
* choco install mingw
* choco install openjdk
* choco install nvm (or use nodejs.installfor latest version)
* nvm install latest
* nvm install 14.16
* choco install python
* choco install golang
* choco install dotnet-sdk (.NET 5)
* choco install dotnetcore-sdk (.NET Core 3.1)
* choco install codeblocks
* choco install sourcetree
* choco install notepadplusplus
* choco install vscode
* choco install dotultimate --params "'/PerMachine'"
* choco install webstorm --params "/InstallDir:C:\Program Files"
* choco install postman

# Install Desktop util
* choco install rainmeter
* Install rainformer_hwinfo.rmskin
* Add widget
  * Clock
  * CPU
  * GPU
  * Disk
  * Network

# Install Disk util
* uiso97pes.exe + ultraiso.txt
* MiniTool_Partition_Wizard_Technician_Full_v12.3-RSLOAD.NET-.exe

# Install Document util
* mobireadersetup.msi
* creator.msi
* choco install calibre
* choco install foxitreader --ia '/MERGETASKS="!desktopicon /COMPONENTS=*pdfviewer,*ffse,*installprint,*ffaddin,*ffspellcheck,!connectedpdf"'

# Install Internet Browser
* choco install googlechrome
* choco install firefox
* choco install vivaldi

# Install Download Manager
* choco install qbittorrent
* idman638build18f.exe + I.D.M.6P9tch.V21.rar

# Install Media Player
* choco install asio4all
* choco install foobar2000
* DarkOne310build20140207.exe 
* copy ProgramComponent => Program File (x86)/foobar2000/components
* copy foobar2000 => Appdata/Roaming
* choco install k-litecodecpackmega

# Install Media Editor
* dMC-R17.3-Ref-Registered.exe
* choco install subtitleedit

# Install System util
* cctrialsetup.exe + key.txt
* Extract SysinternalsSuite.zip + Add to path

# Install Other util
* choco install 7zip
* choco install bulkrenameutility
* choco install cheatengine (optional)
* choco install hashtab
* choco install hwinfo
* choco install hwmonitor
* choco install msiafterburner
* choco install hxd
* choco install latencymon
* choco install logitechgaming (optional)
* Logitech G Hub
* choco install mediatab
* choco install rufus
* choco install spek
* choco install stellarium
* choco install winrar
* choco install unikey
* choco install steam-client

# Login and sync OneDrive

# Customize Taskbar

# Delete temp file

# Add ICC profile
* B156HAN09.2 #1 2021-03-18 11-33 D6500 2.2 F-S XYZLUT+MTX.icm
* B156HAN09.2 #1 2021-03-26 20-14 D6500 2.2 F-S XYZLUT+MTX.icm
