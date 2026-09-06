# nxcspray
Simple bash script to spray known credentials against multiple services with netexec (https://www.netexec.wiki/)

Originally written by NTHSec (https://github.com/NTHSec/nxcspray)

Forked to add the functionality of authentication checks via NTLM hashes.

# Installation
Clone this repo or download the script directly.

Add the script to /usr/local/bin/ to execute it from anywhere on your machine, or use it in a local directory of your choice.
```
sudo mv ~/Downloads/nxcspray /usr/local/bin
chmod +x /usr/local/bin/nxcspray
```

# Usage
```
└─$ nxcspray -h                 
[-] nxcspray <protocols|all> <targets> -u <username> -p <password>
[-] nxcspray <protocols|all> <targets> -u <username> -H <hash>
```

Example Usage
```bash
nxcspray smb,winrm targets.txt -u e.hills -p 'Il0vemyj0b2025!'
```
<img width="1249" height="172" alt="image" src="https://github.com/user-attachments/assets/1d782a78-1e65-4483-8722-b602c1c1b774" />



```bash
nxcspray all 10.1.45.200 -u e.hills -p 'Il0vemyj0b2025!'
```
<img width="1315" height="365" alt="image" src="https://github.com/user-attachments/assets/65453924-98c5-44c1-975c-bfb40968ef88" />

```bsah
nxcspray smb,ldap 10.10.10.10 -u Administrator -H '13b29964cc2480b4ef454c59562e675c'
```

