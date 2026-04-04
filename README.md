# nxcspray
Simple bash script to spray known credentials against multiple services with netexec (https://www.netexec.wiki/)

# Installation
Clone this repo or download the script directly.

Add the script to /usr/local/bin/ to execute it from anywhere on your machine, or use it in a local directory of your choice.
```
git clone https://github.com/sidsherrill1/nxcspray.git && cd nxcspray
sudo mv nxcspray /usr/local/bin
chmod +x /usr/local/bin/nxcspray
```

# Usage
```
└─$ nxcspray -h                 
[-] Usage: /usr/local/bin/nxcspray <protocols|all> <targets> -u <username> (-p <password> | -H <ntlm_hash>)
```

Example Usage
```
nxcspray smb,winrm targets.txt -u e.hills -p 'Il0vemyj0b2025!'
```
<img width="1249" height="172" alt="image" src="https://github.com/user-attachments/assets/1d782a78-1e65-4483-8722-b602c1c1b774" />



```
nxcspray all 10.1.45.200 -u e.hills -p 'Il0vemyj0b2025!'
```
<img width="1315" height="365" alt="image" src="https://github.com/user-attachments/assets/65453924-98c5-44c1-975c-bfb40968ef88" />



```
nxcspray smb,ldap,winrm hosts.txt -u bob -H aad3b435b51404eeaad3b435b51404ee:5fbc3d5fec8206a30a0e5adb2efe0ecd
nxcspray rdp 10.0.0.5 -u Administrator -H 5fbc3d5fec8206a30a0e5adb2efe0ecd
```
