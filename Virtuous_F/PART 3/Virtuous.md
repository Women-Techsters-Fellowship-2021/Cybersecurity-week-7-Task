
PRACTICAL ACTIVITY 7

 VIRTUOUS FANNY 
virtuous.fanny@womentechsters.org

Part 3: Public key encryption with OpenSSL
What to turn in: A listing of the exact commands you used to accomplish the tasks below.
It is up to you to figure out the exact commands. This time we are using public key cryptography. This is only designed to operate on a small amount of data, so run it on a very small file.
Complete the following tasks:
1.	Generate a RSA private key and save it to a file. The command you should be using is openssl genrsa
2.	Generate and save a corresponding RSA public key. The command needed here is openssl rsa
3.	Encrypt a file using your RSA public key. The command needed is openssl rsautl
4.	Decrypt the file using your RSA private key. Verify that the output matches the original.


SOLUTION


sudo su
nano assign.txt   
openssl genrsa
openssl genrsa -out assignp.pem 2048
openssl rsa -in assignp.pem -pubout -out assignment.pem
cat assignment.pem
openssl rsautl -encrypt -in assign.txt -out assignmentenc.txt -inkey assignment.pem -pubin
ls
cat assignmentenc.txt 
openssl rsautl -decrypt -in assignmentenc.txt -out assignmentdec.txt -inkey assignp.pem 
ls
openssl rsautl -decrypt -in assignmentenc.txt -out assignmentdec.txt -inkey assignp.pem
