## System Information

```sh
$ uname -a

$ uptime

$ timedatectl

$ mount

$ echo $PATH

```

## User Information

```sh
#logged in users
$ w

#show if a user has ever logged in remotely
$ lastlog

$ last

#failed logins
$ failog -a

#local accounts
$ cat /etc/passwd

$ cat /etc/shadow

#groups
$ cat /etc/group

#sudo access
$ cat /etc/sudoers

#accounts with UID 0
$ awk -F: `($3=="0"){print}` /etc/passwd

$ egrep ':0+' /etc/passwd

#view root authorized SSH Auth
$ cat /root/.ssh/authorized_keys

#opened files by user
$ lsof -u <user name>

#root user bash history
$ cat /root/.bash_history

```

## Network Information
> net-tools are obsolete and are replaced by the iproute2 package, net-tools versions are still included as many distros still use them. https://en.wikipedia.org/wiki/Iproute2

**Iproute2 Tools**
```sh
#network interfaces
$ ip addr

#all network connections with PID
$ ss -anp

#tcp connections with additional info
$ ss -tni

#listening ports only with PID
$ ss -lnp

#routes
$ ip route

#arp table
$ ip neigh

#processes listening on ports
$ lsof -i

```

**net-tools**
```sh
#network interfaces
$ ifconfig

#all network connections with PID
$ netstat -anp

#listening ports only
$ netstat -lnp

#routes
$ route

#arp table
$ arp -a

#processes listening on ports
$ lsof -i

```
