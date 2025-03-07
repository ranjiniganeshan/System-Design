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
