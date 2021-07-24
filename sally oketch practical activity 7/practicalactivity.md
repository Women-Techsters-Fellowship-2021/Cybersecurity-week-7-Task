
Part 1
1.	nmap -sP 10.0.2.15/24
2.	nmap -sN 10.0.2.15/24
3.	nmap -sT 10.0.2.15/24
4.	nmap  -sS  10.0.2.15/24
5.	nmap  -sU 10.0.2.15/24
6.	nmap  -sF 10.0.2.15/24
7.	nmap --script vuln 10.0.2.15/24 -p 1-1000  brings a vulnerability that does not allow trial of another account.

part 2
the decrypted hash is: jrahyn+




Part 3
1.	openssl genrsa -out pri.pem 2048
2.	openssl rsa -in pri.pem -pubout -out pub.pem
3.	openssl rsautl -encrypt -in pract7.txt -out encpract7.txt -inkey pub.pem -pubin
4.	openssl rsautl -decrypt -in encpract7.txt -out decpract7.txt -inkey pri.pem   
