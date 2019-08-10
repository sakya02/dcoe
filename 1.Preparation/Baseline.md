# DCOE Baseline hardening guide (WIP)

Follow the recommendations in this article [Penetration Testers’ Guide to Windows 10 Privacy & Security](https://hackernoon.com/the-2017-pentester-guide-to-windows-10-privacy-security-cf734c510b8d) article if they apply.

Be advised the article is a little outdated and some things may no longer be compatible with the latest version of windows or some recommendations could've have changed in light of recent security incidents. DO YOUR RESEARCH AND HAVE GOOD BACKUPS!

## Further recommendations

#### Linux-like package management with Chocolatey

https://chocolatey.org/install

* CLI interface
* Good way to install and keep certain software packages updated. 
* Packages go through a review process.
* Resists MITM attacks by checking hashes before install.
* can be set to automatically check for updates through a scheduled task.

#### Suggested software for DCOE

|Software|Description|
|---|---|
|[HashTab](https://chocolatey.org/packages/hashtab)|HashTab provides OS extensions to calculate file hashes. Or if you prefer use the built-in powershell cmdlet Get-FileHash.|
|[Wireshark](https://chocolatey.org/packages/wireshark)|Packet analysis tool. If installed through chocolatey you may need to also install winpcap separately.|
|[Winpcap](https://chocolatey.org/packages/WinPcap)|Needed if not installed automatically by wireshark.|
|[Putty](https://chocolatey.org/search?q=putty)|or whatever your preferred SSH client is.|
|[winscp](https://chocolatey.org/search?q=winscp)|SFTP client, SCP client, FTPS client and FTP client for Windows.|
|[Sysinternals Suite](https://docs.microsoft.com/en-us/sysinternals/downloads/sysinternals-suite)|if you don't know what this is you don't belong here... jk.. lol... no but seriously|
|[CyberChef](https://gchq.github.io/CyberChef/)|A simple, intuitive web app for analysing and decoding data without having to deal with complex tools or programming languages. CyberChef encourages both technical and non-technical people to explore data formats, encryption and compression.|
|[Nmap](https://chocolatey.org/packages/nmap)|Free and open source utility for network discovery and security auditing.|
|[notepad++](https://chocolatey.org/packages?q=notepad%2B%2B)|Advanced notepad for non-noobs|
|[sublime text](https://chocolatey.org/packages/SublimeText3)|For the enlightened|
|[Process Explorer](https://chocolatey.org/packages/procexp)|Better than task manager|
|[WSUS Offline Update](https://chocolatey.org/packages/wsus-offline-update)|Update windows without an internet connection.|
|[]()||

#### Useful Links

|Link|Description|
|---|---|
|[Hybrid Analysis](https://www.hybrid-analysis.com/)|Free malware analysis service for the community that detects and analyzes unknown threats using a unique Hybrid Analysis technology.|
