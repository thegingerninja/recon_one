# Recon One - Nmap Helper

A bash script to run a basic set of Nmap scans. It is assumed you have a system
with bash and Nmap installed.

1. nmap --top-ports 100
2. nmap -p-
3. nmap -sC -sV (on found open ports)
4. nmap -sU (on nmap default udp ports)

-Pn is added if needed after a ping ttl is analysed. 

The resulting files are saved in a directory named after the target IP address.

## Usage

```
 (                         )              
 )\ )                   ( /(              
(()/(  (                )\())         (   
 /(_))))\ (  (   (     ((_)\   (     ))\  
(_)) /((_))\ )\  )\ )    ((_)  )\ ) /((_) 
| _ (_)) ((_|(_)_(_/(   / _ \ _(_/((_))   
|   / -_) _/ _ \ ' \)) | (_) | ' \)) -_)  
|_|_\___\__\___/_||_|   \___/|_||_|\___|  

Usage: ./recon_one remote_host

e.g. ./recon_one 127.0.0.1
```

### Has the server been reset?

When the script runs it will ask if the server needs reset.  CTF servers can be
left in a mess by other hackers so it's often a good idea to reset the server
first if allowed.

### Do you want to include UDP scans?

The UDP scans can take a long time to run so there is a choice.  If yes, then the
UDP scan will be done after the other TCP scans.


## Disclaimer

Do not run this script if you have no idea what Nmap is and have no idea of the laws
around running port scans. Only run this script on machines you have full permission
to port scan.  Port scanning a machine you do not own and do not have written
permission to scan could get you into serious trouble.

