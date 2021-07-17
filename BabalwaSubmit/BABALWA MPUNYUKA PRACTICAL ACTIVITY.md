# PART 1 ANSWERS
1. ping google.com
2. nmap -sP 192.168.56.1/24
3. nmap -sT 192.168.56.1/24
4. nmap -sS 192.168.56.1
5. NMAP -sU local host
6.
7.nmap -p 1-1000 -sV --script=vulners

# PART 2 ANSWERS

# PART 3 ANSWERS
1. openssl genrsa -out privatekey.pem 2048
# Generated the privatekey using the command above.

2. openssl rsa -in pkey.pem -pubout -out public1.pem
# Seperated the public key and saved it to a file called public1.pem

3. openssl rsautl -encrypt -n msg.txt -out msg2.txt -inkey public1.pem -pubin
# encrypted a file msg.txt and saved the output to a file called msg2.txt

4. openssl rsautl -decrypt -in msg2.txt -out finals.txt -inkey pkey.pem
# Decrypted the file msg2.txt and saved it in a file called finals.txt

