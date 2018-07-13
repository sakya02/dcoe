## System Information

```
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

C:\> netstat -nr

C:\> netstat -vb

C:\> nbtstat -S

C:\> route print

C:\> arp -a

C:\> ipconfig /displaydns

C:\> netsh winhttp show proxy

C:\> ipconfig /allcompartments /all

C:\> netsh wlan show interfaces

C:\> netsh wlan show all

C:\> reg query "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\Connections\WinHttpSettings"

C:\> type %SYSTEMROOT%\system32\drivers\etc\hosts

C:\> wmic nicconfig get descriptions,IPaddress,MACaddress

C:\> wmic netuse get name,username,connectiontype,localname





```
