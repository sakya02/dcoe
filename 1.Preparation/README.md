# Preparation
> The baseline actions needed to ensure proper environmental hygiene. Many of these steps occur as a part of the organization's security operations apparatus and represent the ongoing efforts to make the environment defensible and investigable.
Ref. [SANS Sec504](https://www.sans.org/course/hacker-techniques-exploits-incident-handling)

## Training
### CTF
|Site|Description|
|---|---|
|[Overthewire](http://overthewire.org/wargames/)|The wargames offered by the OverTheWire community can help you to learn and practice security concepts in the form of fun-filled games.|
|[Vulnhub](https://www.vulnhub.com/)|An extensive  collection of vulnerable VMs with user-created solutions.|
|[Hack The Box](https://www.hackthebox.eu/)|Hack The Box is an online platform allowing you to test your penetration testing skills and exchange ideas and methodologies with other members of similar interests. In order to join you should solve an entry-level challenge.|
|[Pwnable.tw](https://pwnable.tw/)|Pwnable.tw is a wargame site for hackers to test and expand their binary exploiting skills.|
|[Pwnable.kr](http://pwnable.kr/)|A non-commercial wargame site which provides various pwn challenges regarding system exploitation.|
|[Counterhack](https://www.counterhackchallenges.com/)|SANS NetWars|
|[Holiday Hack Challenge](https://holidayhackchallenge.com/)|SANS sponsored annual hacking challenges|
|[]()||
|[]()||
|[]()||
|[]()||
|[]()||

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

## Jump Bag

Coming soon

## IR Policy Procedure

* [Cyber Kill Chain](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html) Framework developed by Lockheed Martin
