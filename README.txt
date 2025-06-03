This is a complilation of projects completed for my Security Information & Assurance class taken at CSU East Bay. 
These projects look into how various applications and exploits can affect users. This focuses on the five security 
principles of data confidentiality, data integrity, access control, authentication, and non-repudiation.

#Assignment 1:
This project examined network traffic on a virtual machine by generating both encrypted and unencrypted traffic. 
Unencrypted packets were sent between a client and host server, and a connection was established to an unencrypted 
website generated using python. All packets were captured and analyzed to see what information could be accessed by a 
third party. The results indicate that most data is visible to other users on the network when the traffic is unencrypted.

#Assignment 2:
This project uses the encryption provided by GPG to complete both symmetric encryption using a password when prompted 
as well as the asymmetric encryption using a provided public key and using GPG to generate a new key with a prompted 
password. The file is then signed using a private key. These methods are used to encrypt a simple text file and send 
it through Netcat, intercepting it with WireShark the data is encrypted and therefore not accessible without knowing 
the key or encryption method. This proved to be a much safer method to send data across networks without losing data 
confidentiality and since the file is signed it also ensures authentication and non-repudiation. After this, Steghide 
is used to embed the original text file into an image file. Furthermore, md5 is used to find the size of both the 
original and the embedded image files. Upon comparison it is evident that the image integrity is compromised as the 
embedded file size is larger than the original. Additionally, renaming the original image and comparing the file size 
shows that the file data has not changed and the file is still identical to the original, renaming had no impact.

#Assignment 3:
This project captures and analyzes packets using WireShark, captured from both attempted and successful brute force 
password attacks on an SSH server using Hydra. In this experiment the user’s login is known and a list of roughly 300 
common passwords are attempted, after roughly 250 the correct password is entered and Hydra returns a statement saying 
it is the correct password and the program terminates. Upon inspection of the packets you can see that the Diffie-Hellman 
key exchange algorithm is used and is clearly shown in plaintext. However, it is extremely difficult to tell the 
difference between successful password attempts and unsuccessful attempts. The main difference can be found in the 
size and length of the subsequent packets, with failed attempts having many more small packets sent back and forth. 
From this we can see both the vulnerabilities to brute force attacks for common passwords as well as show the strength 
and possible vulnerabilities of the encrypted communication.

#Assignment 4:
This project explores the use of iptables firewalls to control and manipulate network traffic. Focusing on creating, 
blocking, and redirecting traffic to and from two virtual machines. Additionally, the limitations of mac address 
filtering as a security measure are demonstrated and analyzed. Traffic redirection to a local web server is also tested, 
and used to see the impact of blocking specific devices. It becomes apparent that mac address filtering is not a secure 
method of access control as mac address spoofing is incredibly easy to perform. However, filtering traffic by IP 
addresses is proven to be fairly secure and even allows the ability to block all IP addresses under the same subnet 
mask. Packet analysis using WireShark highlights the availability of communications along SSH servers, HTTP pages, 
and network traffic with firewall interference. The findings reveal the strengths and limitations of firewalls as it 
applies to the five main security service categories.

#Assignment 5:
This assignment demonstrates the capabilities of tools such as Nmap, Zenmap, and Wireshark, to scan and analyze 
network configurations as well as perform security audits by capturing packets sent between a Kali Linux virtual 
machine and an Ubuntu virtual machine. After enabling network services on Ubuntu, scanning and packet analysis were 
conducted to explore how these tools operate, collect data, and reveal network service details. The activity demonstrates 
the availability of network information available to attackers as well as helps to locate the insecurities of the 
Ubuntu machine.

#Assignment 6:
This assignment sets up a honeypot server in a virtual machine by disabling the firewall. We then proceed to attack 
this from a separate virtual machine over a network using five different network services. These were HTTP, FTP, SSH, 
SMTP, and Telnet traffic. All communications and attackers were recorded in logs by the honeypot server. In addition to 
this we wrote two python scripts to create two more, more sophisticated imitations of network services, HTTP on port 
8080 and an echo server on port 9009. From these we can tell the breadth and depth of information a honey pot server 
is able to record, exposing attackers ip addresses and methods in plaintext.

#Assignment 7:
This assignment explores the use of the Tor browser over an onion network. We capture packets of the generated network 
traffic only to discover very little regarding the content of the data being sent back and forth.
