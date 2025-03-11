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



## How to Design the CIDR range for VPC.
* Classless Inter-Domain Routing : CIDR is a system that allows for a flexible allocation of IP addresses
* CIDR notation (e.g., 192.168.1.0/24) combines an IP address with a prefix length that indicates the number of bits used for the network portion.

# How It Works:
* The suffix (like “/24”) determines how many addresses are available in the network. For example, a /24 network provides 256 IP addresses (with typically 254 usable for hosts)
* Ipaddress are 32 bits. 
* 10.0.0.8 ->
* 1286432168421 -> Each octet is represented in powers of 2
* 00001010.00000000.00000000.00001000


## Private IP Ranges Defined by RFC 1918
* 10.0.0.0/8
1. Range: 10.0.0.0 to 10.255.255.255
This range is very large and is well-suited for large organizations or service providers that need to segment their network extensively. It offers a high degree of flexibility in terms of subnetting, allowing you to design a complex hierarchical network.

* 172.16.0.0/12
Range: 172.16.0.0 to 172.31.255.255
Usage:
1. This block is typically used by medium-sized organizations. It provides a balance between the vast address space of the 10.0.0.0/8 block and the smaller 192.168.0.0/16 block. It’s a good option if you need more addresses than a home or small office network but don’t require the full 10/8 space.
   
* 192.168.0.0/16
Range: 192.168.0.0 to 192.168.255.255
Number of Addresses: 65,536 addresses
1. Usage:
This range is most commonly used in small networks, such as home networks and small offices. Many consumer-grade routers are preconfigured to use subnets within this range (e.g., 192.168.1.0/24). Its smaller size makes it easier to manage for less complex networks.

* In a CIDR notation like 10.0.0.0/8, the "/8" tells you how many bits in the 32-bit IP address are dedicated to the network portion. Here's a breakdown:

# Network and Host Portions
* Network Portion (/8):
The /8 means that the first 8 bits of the IP address are fixed to represent the network.
For 10.0.0.0/8, this means that the first octet is 10 (which in binary is 00001010), and it remains the same for every address in this network.
Host Portion:
The remaining 32 - 8 = 24 bits are used for host addresses within the network.
This gives you a total of 2^24 = 16,777,216 possible IP addresses (from 10.0.0.0 to 10.255.255.255).
What Changes and What Remains Fixed
Fixed Part (Network):
10.0.0.0/8 fixes only the first octet. Every IP in this block starts with 10.
Variable Part (Host):
The remaining three octets can vary from 0.0.0 up to 255.255.255, allowing for a vast number of unique addresses within this network.





