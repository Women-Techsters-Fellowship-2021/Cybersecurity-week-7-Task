# Practical Activity 7
## Sally Mukami Kagai
#### sally.mukami@womentechsters.org
## Part 1
1. I used the *nmap -PE* command to send ICMP ECHO packets and i wanted to discvover all the hosts on my local network since i did not know which one was active.
2. For the TCP ping command, i utilize  the TCP ACK packet that i send to the host. The flag sends an ACK packet to port80 by default. Command used is *nmap -PT*
3. the TCP Connect Scan we send SYN packets to the target and the machine replys with a SYN/ACK packet. Command used is *nmap -sT*
4. The Stealth scan is used by the port scanner when no scan option is defined. Command is  *nmap -sS*
5. The UDP scan evaluates the UDP ports on the target system. Command used *nmap -sU*
6.
6. I made use of the -sP fin scan to scan the FIN flag only. ?*nmap -sP*
7. To check for vulnerabilities on the computer i performed a scan of all tge nmap scripts and took special interest on the ftp-vuln-cve script. The script checks for a stack-based buffer overflow in the ProFTPD server, version between 1.3.2rc3 and 1.3.3b. By sending a large number of TELNET_IAC escape sequence, the proftpd process miscalculates the buffer length, and a remote attacker will be able to corrupt the stack and execute arbitrary code within the context of the proftpd process (CVE-2010-4221). On running the script on port 21 there were no evident vulnerabilities on the system

## Part 2 Cracking Hash
I used the SHA-1 conversion and reverse lookup and the SHA-1 hash was successfully reversed into the string **jrahyn+**

## Part 3 Public key encryption with OpenSSL
1. Create a directory called part3, and generated a key and named it part3.pem. The text message to be encrypted is on the file called message.
2. Seperated the private and the public keys and named the public key *part3public.pem*
3. Encrypted the message text and saved it as *enc*
4. Decrypted the file and saved the output to *decrypt*