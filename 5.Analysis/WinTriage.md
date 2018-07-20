## System Information

```batch
#obvious
C:\> echo %DATE% %TIME%

PS C:\> Get-Date

C:\> hostname

C:\> systeminfo

C:\> systeminfo | findstr /B /C:"OS Name" /C:"OS Version"

PS C:\> Get-ComputerInfo

C:\> wmic csproduct get name

C:\> wmic bios get serialnumber

C:\> wmic computersystem list brief

C:\> wmic product get name,version

C:\> echo %PATH%

# need psinfo from sysinternals
C:\> psinfo -accepteula -s -h -d

```

## User Information

```
C:\> whoami

C:\> net users

C:\> net localgroup administrators

C:\> net group administrators

C:\> wmic rdtoggle list

C:\> wmic useraccount list

C:\> wmic group list

C:\> wmic netlogin get name,lastlogin,badpasswordcount

C:\> wmic netclient list brief

C:\> doskey /history > history.txt

```

## Network Information

```
#ethernet statistics
C:\> netstat -e

#numerical, all connections, owning process and executable
C:\> netstat -naob

#show only ports listening
C:\> netstat -naob | find "LISTENING"

#established connections
C:\> netstat -naob | find "ESTABLISHED"

#watch for connections every second
C:\> netstat -naob 1 | find "<IP ADDR or PORT>"

#display routing table information
C:\> netstat -nr

#display sequence of components involved with creating connection
C:\> netstat -vb

#per protocol statistics
C:\> nbtstat -S

#same as netstat -nr
C:\> route print

#display arp entries
C:\> arp -a

#dns cache
C:\> ipconfig /displaydns

#exactly what it says
C:\> netsh winhttp show proxy

C:\> ipconfig /allcompartments /all

C:\> netsh wlan show interfaces

C:\> netsh wlan show all

#i dont know how useful this is, might remove
C:\> reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\Connections\WinHttpSettings"

#show hosts file
C:\> type %SYSTEMROOT%\system32\drivers\etc\hosts

C:\> wmic nicconfig get description,IPaddress,MACaddress

C:\> wmic netuse get name,username,connectiontype,localname

```

## Service information

```posh

C:\> tasklist

C:\> tasklist /svc

C:\> tasklist /svc /fi "imagename eq svchost.exe"

C:\> tasklist /svc /fi "pid eq <PID>"

C:\> schtasks

C:\> net start

C:\> sc query

C:\> wmic service list brief | findstr "Running"

C:\> wmic service list config

C:\> wmic process list brief

C:\> wmic process list status

C:\> wmic process list memory

C:\> wmic job list brief

PS C:\> Get-Service | Where-Object {$_.Status -eq "running"}

#list all processes and then all loaded modules
PS C:\> Get-Process | select modules | Foreach-Object{$_.modules}

```

## Policy, Patch and Settings Information

```
#list system variables
C:\>set

C:\> gpresult /r

C:\> gpresult /z > <filename>.txt

C:\> gpresult /H report.html /F

#quick fix engineering
C:\> wmic qfe

#GPO installed software
C:\> reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Group Policy\AppMgmt"

```

## Autorun Information

```
C:\> wmic startup list full

C:\> wmic ntdomain list brief

#view contents of startup folder
C:\> dir "%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Startup"

#old xp
C:\> dir "%SystemDrive%\Documents and Settings\All Users\Start Menu\Programs\Startup"

C:\> dir "%USERPROFILE%\Start Menu\Programs\startup

C:\>


```
