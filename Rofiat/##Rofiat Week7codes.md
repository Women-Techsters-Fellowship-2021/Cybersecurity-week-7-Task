##Rofiat Week7codes
## Week7 Codes
# PART 1 ANSWERS 
1. Icmp ping
   nmap -pP 10.0.2.15/24
2  TCP ping
   nmap -sP 10.0.2.15
3  TCP connect
   nmap -sT 10.0.2.15
4  Stealth scanning
   sudo nmap -sS 10.0.2.15
5  UDP
   sudo nmap -sU 10.0.2.15
6  Stealth FIN
   nmap -sF 10.0.2.15
7  Vulnerabilities within host network
   nmap -Pn --script vuln 192.168.56.1
   CVE:CVE-2007-6750 slowloris DOS attack tries to keep many connections to the web server open and on hold them as long as posssible
   It does this by opening connection to the target server and sending partial request.By doing so it starves
   the http web server's respurces causing Denial o services.

# PART 2 ANSWERS
  jrahyn+

# PART 3 ANSWERS
1. openssl genrsa -out rsa.private 1024
   The private key is generated and saved in rsa.private with the private key size 1024 bits
2. openssl rsa -in rsa.private -out rsa.public -pubout -outform PEM
   The public key i saved in rsa.public file 
3  openssl rsautl -in pass.txt -out pass.enc -pubin -inkey rsa.public -encrypt
4  openssl rsautl -in pass.enc -out pass.dec -inkey rsa.private -decrypt