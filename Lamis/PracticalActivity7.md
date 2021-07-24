**Practical Activity 7**

**Part 1: based on port scanning using Nmap**

*Perform the following scans on your Kali linux machine and attach the code and output of each command.*

1-Icmp ping          nmap -sP -PI 10.0.2.0/24               

2-tcp ping           nmap -sn -PS 10.0.2.0/24    (SYN) / nmap -sn -PA 10.0.2.0/24  (SYN)                  

3-TCP connect        nmap -sT -n -Pn 10.0.2.15   --top-ports 10   

4-Stealth Scanning   nmap -sS -n 10.0.2.15       --top-ports 10        

5-UDP Scanning       nmap -sU  -n 10.0.2.15       

6-Stealth FIN        nmap -sF  -n 10.0.2.15

7-Find any Vulnerabilities within your host network using 
vuln --script and give short description on how to exploit that vulnerability.        nmap  --script vuln 10.0.2.15


**Part 2: Cracking a Hash using whatever tool you are comfortable with.** 

*Part 2: Cracking a Hash using whatever tool you are comfortable with and screenshot the answer.*

1-using :https://hashes.com/en/decrypt/hash

 06f8aa28b9237866e3e289f18ade19e1736d809d                       jrahyn+

**Part3: Encryption with OpenSSL**

1-Generate a RSA private key and save it to a file. The command you should be using is openssl genrsa  

openssl genrsa -out keypar1.pem 2048


2-Generate and save a corresponding RSA public key. The command needed here is openssl rsa

openssl rsa -in keypar1.pem -pubout -out public.pem


3-Encrypt a file using your RSA public key. The command needed is openssl rsautl 

openssl rsautl -encrypt -in Enc.txt -out encrypt.txt -inkey public.pem -pubin


4-Decrypt the file using your RSA private key. Verify that the output matches the original.

openssl rsautl -decrypt -in encrypt.txt -out decrypt.txt -inkey keypar.pem

