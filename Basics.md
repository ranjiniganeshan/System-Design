# How does DNS works?

* DNS, or the Domain Name System, works like an internet phone book. When you type a website address (like example.com) into your browser, DNS translates that human-friendly name into an IP address, 
which is the numeric address computers use to communicate with each other. 
* Step 1: Your computer → DNS Resolver
(The resolver already knows which root servers to use.)

* Step 2: DNS Resolver → Root Nameserver
(Root nameserver returns a referral to the correct TLD nameserver.)

* Step 3: DNS Resolver → TLD Nameserver
(TLD nameserver returns a referral to the authoritative nameserver.)

* Step 4: DNS Resolver → Authoritative Nameserver
(Authoritative nameserver returns the final IP address.)

![DNS drawio](https://github.com/user-attachments/assets/cc20687a-11c3-47ce-b038-2652866a0c04)

How Does https work?
![image](https://github.com/user-attachments/assets/e4c886f6-3425-4a6e-9fdb-18112e1617e1)

How is the data encrypted and decrypted?

Step 1 - The client (browser) and the server establish a TCP connection.

Step 2 - The client sends a “client hello” to the server. The message contains a set of necessary encryption algorithms (cipher suites) and the latest TLS version it can support. The server responds with a “server hello” so the browser knows whether it can support the algorithms and TLS version.

The server then sends the SSL certificate to the client. The certificate contains the public key, hostname, expiry dates, etc. The client validates the certificate. 

Step 3 - After validating the SSL certificate, the client generates a session key and encrypts it using the public key. The server receives the encrypted session key and decrypts it with the private key. 

Step 4 - Now that both the client and the server hold the same session key (symmetric encryption), the encrypted data is transmitted in a secure bi-directional channel.



## learn A record




