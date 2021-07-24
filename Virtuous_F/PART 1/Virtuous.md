
PRACTICAL ACTIVITY 7

 VIRTUOUS FANNY 
virtuous.fanny@womentechsters.org

Part 1: Perform the following scans on your Kali linux machine and attach the code and output of each command.
1.	Icmp ping                     
2.	tcp ping                        
3.	TCP connect                
4.	Stealth Scanning           
5.	UDP Scanning             
6.	Stealth FIN   
7.	Find any Vulnerabilities within your host network using vuln --script     and give short description on how to exploit that vulnerability.          


1. Icmp Ping

   code:
     nmap -p 1-2000 -v -A -sV -PE 10.0.2.15

    output:
         Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-16 10:35 EDT
        Nmap scan report for 10.0.2.15
        Host is up (0.000041s latency).
        Not shown: 1999 closed ports
        PORT   STATE SERVICE
        22/tcp open  ssh

        Nmap done: 1 IP address (1 host up) scanned in 1.28 seconds

2. tcp ping

    code:
        nmap -p 1-2000 -sS 10.0.2.15
    output:
        Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-16 10:38 EDT
        Nmap scan report for 10.0.2.15
        Host is up (0.000031s latency).
        Not shown: 1999 closed ports
        PORT   STATE SERVICE
        22/tcp open  ssh

        Nmap done: 1 IP address (1 host up) scanned in 0.61 seconds

3. TCP connect

    code: 
        nmap -p 1-2000 -sT 10.0.2.15
    output:
        Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-16 10:41 EDT
        Nmap scan report for 10.0.2.15
        Host is up (0.00034s latency).
        Not shown: 1999 closed ports
        PORT   STATE SERVICE
        22/tcp open  ssh

        Nmap done: 1 IP address (1 host up) scanned in 0.57 seconds
                                                             
4. Stealth Scanning 

    code: 
        nmap -p 1-2000 -sN 10.0.2.15 
    output:
        Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-16 10:51 EDT
        Nmap scan report for 10.0.2.15
        Host is up (0.000018s latency).
        Not shown: 1999 closed ports
        PORT   STATE         SERVICE
        22/tcp open|filtered ssh

        Nmap done: 1 IP address (1 host up) scanned in 1.96 seconds

         
5. UDP Scanning             

    code: 
        nmap -p 1-2000 -sU 10.0.2.15

    output:
        Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-16 10:59 EDT
        Nmap scan report for 10.0.2.15
        Host is up (0.000034s latency).
        All 2000 scanned ports on 10.0.2.15 are closed

        Nmap done: 1 IP address (1 host up) scanned in 10.22 seconds

6. Stealth FIN             

    code: 

    output:

7. 	Find any Vulnerabilities within your host network using vuln --script     and give short description on how to exploit that vulnerability.  


        
        Starting Nmap 7.91 ( https://nmap.org ) at 2021-07-16 11:23 EDT


Nmap scan report for 10.0.2.15
Host is up (0.000018s latency).
Not shown: 1999 closed ports
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.4p1 Debian 5 (protocol 2.0)
| vulners: 
|   cpe:/a:openbsd:openssh:8.4p1: 
|       EDB-ID:21018    10.0    https://vulners.com/exploitdb/EDB-ID:21018  *EXPLOIT*
|       CVE-2001-0554   10.0    https://vulners.com/cve/CVE-2001-0554
|       MSF:ILITIES/GENTOO-LINUX-CVE-2021-28041/        4.6     https://vulners.com/metasploit/MSF:ILITIES/GENTOO-LINUX-CVE-2021-28041/      *EXPLOIT*
|       CVE-2021-28041  4.6     https://vulners.com/cve/CVE-2021-28041
|       MSF:ILITIES/OPENBSD-OPENSSH-CVE-2020-14145/     4.3     https://vulners.com/metasploit/MSF:ILITIES/OPENBSD-OPENSSH-CVE-2020-14145/   *EXPLOIT*
|       MSF:ILITIES/HUAWEI-EULEROS-2_0_SP9-CVE-2020-14145/      4.3     https://vulners.com/metasploit/MSF:ILITIES/HUAWEI-EULEROS-2_0_SP9-CVE-2020-14145/*EXPLOIT*
|       MSF:ILITIES/HUAWEI-EULEROS-2_0_SP8-CVE-2020-14145/      4.3     https://vulners.com/metasploit/MSF:ILITIES/HUAWEI-EULEROS-2_0_SP8-CVE-2020-14145/*EXPLOIT*
|       MSF:ILITIES/HUAWEI-EULEROS-2_0_SP5-CVE-2020-14145/      4.3     https://vulners.com/metasploit/MSF:ILITIES/HUAWEI-EULEROS-2_0_SP5-CVE-2020-14145/*EXPLOIT*
|       MSF:ILITIES/F5-BIG-IP-CVE-2020-14145/   4.3     https://vulners.com/metasploit/MSF:ILITIES/F5-BIG-IP-CVE-2020-14145/ *EXPLOIT*
|_      CVE-2020-14145  4.3     https://vulners.com/cve/CVE-2020-14145
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 13.11 seconds
