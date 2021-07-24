**WEEK 7: Practical Activity**

- Part 1: based on port scanning using nmap
- Part 2: Cracking a hash using whatever tool you are comfortable with
- Part 3: Encryption with OpenSSL

**Part 1: Perform the following scans on your Kali Linux machine and attach the code and output of each command.**

1. ICMP ping: **sudo nmap -sP -PE 10.0.2.15/24**

![part1_1](./week_7_practical_acitivity/part1_1.png)

2. TCP ping: **nmap -p 389 10.0.2.15/24**

![part1_2](./week_7_practical_acitivity/part1_2.png)

3. TCP connect: **nmap -sT 10.0.2.15**

![part1_3](./week_7_practical_acitivity/part1_3.png)

4. Stealth scanning: **sudo nmap -sS 10.0.2.15**

![part1_4](./week_7_practical_acitivity/part1_4.png)

5. UDP scanning: **sudo nmap -sU 10.0.2.15**

![part1_5](./week_7_practical_acitivity/part1_5.png)

6. Stealth FIN: **sudo nmap -sF 10.0.2.15**

![part1_6](./week_7_practical_acitivity/part1_6.png)

7. Find any vulnerabilities within your host network using vuln -script and give a short description on how to exploit that vulnerability
**sudo nmap -v -script vuln 192.168.56.1**

![part1_7](./week_7_practical_acitivity/part1_7.png)

![part1_7_2](./week_7_practical_acitivity/part1_7_2.png)

I have received the \_samba-vuln-cve-2012-1182 error which checks if the target machines are vulnerable to Samba heap overflow hence allows remote code execution as the &quot;root&quot; user from an anonymous connection.

**Part 2: Cracking a hash using whatever tool you are comfortable with and screenshot the answer**

I used [SHA-1 reverse for 06f8aa28b9237866e3e289f18ade19e1736d809d (gromweb.com)](https://sha1.gromweb.com/?hash=06f8aa28b9237866e3e289f18ade19e1736d809d) to convert the SHA-1 Hash to a string. The decrypted value was **jrahyn+**

![part2_1](./week_7_practical_acitivity/part2_1.png)

**Part 3: Public key encryption with OpenSSL**

Create a file called testfile.txt which contains the text &#39;testfile&#39; using **echo testfile \&gt; testfile1.txt**

![part3_1](./week_7_practical_acitivity/part3_1.png)

![part3_1_2](./week_7_practical_acitivity/part3_1_2.png)

Generate a private key using **openssl genrsa -out privatekey.pem 2048** to generate a private key called privatekey.pem. This is the private key that will be used to decrypt the file later on.

![part3_1_3](./week_7_practical_acitivity/part3_1_3.png)

Generate a corresponding public key from the privatekey.pem using **openssl rsa -in privatekey.pem -pubout -out publickey.pem**

![part3_2](./week_7_practical_acitivity/part3_2.png)

Encrypt testfile1.txt (the file created in the first step) to a file called encryptedfile.txt which will be the encrypted file created using **openssl rsautl -encrypt -in testfile.txt -out encryptedfile.txt -inkey publickey.pem -pubin**. We will use the publickey.pem as the key used to lock the file.

![part3_3](./week_7_practical_acitivity/part3_3.png)

If you check the encrypted files contents, it should look like gibberish.

![part3_3_2](./week_7_practical_acitivity/part3_3_2.png)

Fifth, to decrypt encryptedfile.txt, use **openssl rsautl -decrypt -in encryptedfile.txt -out decryptedfile.txt -inkey privatekey.pem** which will give a decrypted file called decryptedfile.txt.

![part3_4](./week_7_practical_acitivity/part3_4.png)

If you check out the content of decryptedfile.txt, it will be identical to the information to testfile.txt

![part3_4_2](./week_7_practical_acitivity/part3_4_2.png)
