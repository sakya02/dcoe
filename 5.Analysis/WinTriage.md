# System Information

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
