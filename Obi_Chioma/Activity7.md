# Part 1: Perform the following scans on your Kali linux machine and attach the code and output of each command. 

1. Icmp ping
   Answer: nmap -sP 10.0.2.15/24                   

2. tcp ping  
   Answer: sudo nmap -sN 10.0.2.15/24                       

3. TCP connect  
   Answer: nmap -sT 10.0.2.15/24               

4. Stealth Scanning    
   Answer: nmap -sS 10.0.2.15/24        

5. UDP Scanning 
   Answer: map -sU 10.0.2.15/24             

6. Stealth FIN    
   ANswer: nmap -sF 10.0.2.15/24

7. Find any Vulnerabilities within your host network using vuln --script     and give short description on how to exploit that vulnerability.          
   Answer: nmap --script vuln 10.0.2.15/24 -p 1-1000

# Part 2: Cracking a Hash using whatever tool you are comfortable with and screenshot the answer.  

A hacker leaked the below hash online. Can you crack it to know the password of the CEO? the flag is the password Hash: 06f8aa28b9237866e3e289f18ade19e1736d809d 

 Use https://www.dcode.fr/hash-function to find its a SHA1 hash, then i used https://md5hashing.net/hash/sha1/06f8aa28b9237866e3e289f18ade19e1736d809dto decrypt to get the password as jrahyn+ l

# Part 3: Public key encryption with OpenSSL 

What to turn in: A listing of the exact commands you used to accomplish the tasks below. 
It is up to you to figure out the exact commands. This time we are using public key cryptography. This is only designed to operate on a small amount of data, so run it on a very small file. 
Complete the following tasks: 

I created a text file named PracticalActivity7.txt using the command touch PracticalActivity7.txt 

1. Generate a RSA private key and save it to a file. The command you should be using is openssl genrsa 
Answer: openssl genrsa -out privatekey.pem 2048

2. Generate and save a corresponding RSA public key. The command needed here is openssl rsa 
Answer: openssl rsa -in privatekey.pem -pubout -out publickey.pem

3. Encrypt a file using your RSA public key. The command needed is openssl rsautl 
Answer: openssl rsautl -encrypt -in PracticalActivity7.txt -out EncryptedPract7.txt -inkey publickey.pem -pubin

4. Decrypt the file using your RSA private key. Verify that the output matches the original.
Answer: openssl rsautl -decrypt -in EncryptedPract7.txt -out decryptedPrac7.txt -inkey privatekey.pem

 