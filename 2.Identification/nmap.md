## Host Discovery - Generate Live Hosts List
```sh
$ nmap -sn -T4 -oG Discovery.gnmap 192.168.56.0/24
$ grep "Status: Up" Discovery.gnmap | cut -f 2 -d ' ' > LiveHosts.txt
```

## Port Discovery - Most Common Ports
> http://nmap.org/presentations/BHDC08/bhdc08-slides-fyodor.pdf
```sh
$ nmap -sS -T4 -Pn -oG TopTCP -iL LiveHosts.txt
$ nmap -sU -T4 -Pn -oN TopUDP -iL LiveHosts.txt
$ nmap -sS -T4 -Pn --top-ports 3674 -oG 3674 -iL LiveHosts.txt
```

## Port Discovery - Full Port Scans (UDP is very slow)
```sh
$ nmap -sS -T4 -Pn -p 0-65535 -oN FullTCP -iL LiveHosts.txt
$ nmap -sU -T4 -Pn -p 0-65535 -oN FullUDP -iL LiveHosts.txt
```

## Print TCP\UDP Ports
```sh
$ grep "open" FullTCP|cut -f 1 -d ' ' | sort -nu | cut -f 1 -d '/' |xargs | sed 's/ /,/g'|awk '{print "T:"$0}'
$ grep "open" FullUDP|cut -f 1 -d ' ' | sort -nu | cut -f 1 -d '/' |xargs | sed 's/ /,/g'|awk '{print "U:"$0}'
```

## Detect Service Version
```sh
$ nmap -sV -T4 -Pn -oG ServiceDetect -iL LiveHosts.txt
```

## Operating System Scan
```sh
$ nmap -O -T4 -Pn -oG OSDetect -iL LiveHosts.txt
```

## OS and Service Detect
```sh
$ nmap -O -sV -T4 -Pn -p U:53,111,137,T:21-25,80,139,8080 -oG OS_Service_Detect -iL LiveHosts.txt
```

# Firewall Avoidance


## fragmentation
```sh
$ nmap -f
```

## change default MTU size number must be a multiple of 8 (8,16,24,32 etc)
```sh
$ nmap --mtu 24
```

## Generates a random number of decoys
```sh
$ nmap -D RND:10 [target]
```

## Manually specify the IP addresses of the decoys
```sh
$ nmap -D decoy1,decoy2,decoy3 etc.
```

## Idle Zombie Scan, first t need to find zombie ip
```sh
$ nmap -sI [Zombie IP] [Target IP]
```

## Source port number specification
```sh
$ nmap --source-port 80 IP
```

## Append Random Data to scan packages
```sh
$ nmap --data-length 25 IP
```

## MAC Address Spoofing, generate different mac for host pc
```sh
$ nmap --spoof-mac Dell/Apple/3Com IP
```

## Brute Force DNS records

```sh
$ nmap --script dns-brute --script-args dns-brute.domain=foo.com,dns-brute.threads=6,dns-brute.hostlist=./hostfile.txt,newtargets -sS -p 80
$ nmap --script dns-brute www.foo.com
```

## Identify WAF

```sh
$ nmap -p 80,443 --script=http-waf-detect 192.168.56.102
$ nmap -p 80,443 --script=http-waf-fingerprint 192.168.56.102
$ wafw00f www.example.com
```

## MS08-067

```sh
$ nmap -v -p 139, 445 --script=smb-check-vulns --script-args=unsafe=1 192.168.31.205
$ searchsploit ms08-067
$ python /usr/share/exploitdb/platforms/windows/remote/7132.py 192.168.31.205 1
```



-Pn to skip ping 


## Scan for vulnerable SMB servers unsafe=1 may cause knockover

```sh
$ nmap -v -p 445 --script=smb-check-vulns --script-args=unsafe=1 192.168.1.X
```

## Search for nmap scripts for keywords
```sh
$ ls /usr/share/nmap/scripts/* | grep ftp
```
