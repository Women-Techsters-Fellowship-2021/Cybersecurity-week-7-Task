1. Perform an Icmp ping  scan on your kali linux                    
## ANSWER 
To Ping input the command  "nmap -sP 10.0.2.0/24" this is my Ip Address


2. Perform a tcp Ping on your kali linux
Answer 
3. To perform a TCP ping I input Nmap  -sT  and my network address which is 10.0.2.0/24 hence giving the command "nmap -sT  10.0.2.0/24"

4. Perform a TCP connect on your kali linux
ANSWER
I changed to  being the root user so as to perform the tcp connect by writing “ SU” command then I input the command “ Nmap  -sT -P  22, 10.0.2.0/24”  to perform a TCP connect. 


5. Perform a STEALTH SCANNING on your Kali linux
ANSWER
We input the command  “nmap -sS 10.0.2.15” this is my IP address

6. Perform a UDP SCANNING on your Kali linux

To perform an UDP scanning  input the command   "nmap -sU 10.0.2.15" this is my Ip address and run it


# A hacker leaked the below hash online. Can you crack it to know the password of the CEO? the flag is the password Hash: 06f8aa28b9237866e3e289f18ade19e1736d809d

ANSWER 
I used the SHA-1 DECODER to identify the CEO Password which is : jrahyn+



1.	Generate a RSA private key and save it to a file. The command you should be using is openssl genrsa

ANSWER 
Use the command  openssl genrsa >private .rsa to generate a private key and run the command
then you can  "cat private.rsa"  to output the contents 


2.	Generate and save a corresponding RSA public key. The command needed here is openssl rsa
ANSWER
Run the command    "openssl rsa -in private.rsa -pubout public.rsa"
then you can "cat public.rsa" to output the contents

3.	Encrypt a file using your RSA public key. The command needed is openssl rsautl
ANSWER
Input the command  "openssl rsaultl -encrypt -inkey public.rsa -in msg.txty -out msg.enc"
NB: msg.txty is my file 

4.	Decrypt the file using your RSA private key. Verify that the output matches the original.

ANSWER
to decrypt a file run the command 
"openssl rsaultl -decrypt -inkey private.rsa -in msg.enc -out msg.dec"


