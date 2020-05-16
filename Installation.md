# My Windows 10 installation

# Create Installation USB
*  en_windows_10_business_editions_version_2004_x64_dvd_d06ef8c5.iso
*  Rufus: GPT-UEFI-NTFS

# Install Windows
*  F12 => USB
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

# Install Drivers
*  1-Chipset_Driver_GH5T3_WN32_10.1.1.18_A04_01.zip
*  1-Intel-Management-Engine-Components-Installer_C3VMM_WIN_11.0.6.1194_A02.zip
*  1-Chipset_Driver_CP3V3_WN32_4.10.67_A00.zip
*  win64_15.33.50.5129.zip
*  392.59-quadro-desktop-notebook-win10-64bit-international-whql.exe
*  PROWinx64.exe
*  WiFi_21.10.1_PROSet64_Win10.exe
*  BT_21.10.1_64_Win10.exe
*  1-Network_Driver_PX8MM_WN64_1.0.0_A00.zip
*  1-Dell-Touchpad-Driver_86M99_WIN_10.3201.101.212_A07.zip
*  Restart

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
    *  Intel Graphic: Balanced, Maximun performance
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