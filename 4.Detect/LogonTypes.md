## Logon Types

### Event ID 4624: An account was succuessfully logged on

|Logon Type|Description|
|Interactive (2)|Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process. Logon at keyboard and screen of system.|
|Network (3)|Intended for high-performance servers to authenticate clear text passwords. LogonUser does not cache credentials for this logon type. (i.e. connection to shared folder on the computer from elsewhere on network)|
|Batch (4)|Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web server. LogonUser does not cache credentias for this logon type.|
|Service (5)|Indicates a service-type logon. The account provided must have the service privileged enabled.|
|Proxy (6)|Indicates a proxy-type logon.|
|Unlock (7)|This logon type is intended for GINA DLLs logging on users who are interactively using the machine. This logon type allows a unique audit record to be generated that shows when the workstation was unlocked|
|NetworkClearText (8)|Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client. This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.|
|NewCredentials (9)|Allows the caller to clone its current token and specify new credentials for outbound connections. The new logon session has the same local identify, but uses different credentials for other network connections.|
|RemoteInteractive (10)|Terminal Services session that is both remote and interactive.|
|CachedInteractive (11)|Attempt cached credentials without accessing the network.|
|CachedRemoteInteractive (12)|Same as RemoteInteractive. This is used for internal auditing.|
|CachedUnlock (13)|Workstation logon.|
