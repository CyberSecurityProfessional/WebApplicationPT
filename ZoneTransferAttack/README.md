# Zone Transfer Attack
* kali@kali:~$ host domain.com
```
domain.com has address 1.2.3.4
domain.com mail is handled by 20 filter1.domain-1.mailguard.com.au.
domain.com mail is handled by 30 filter2.domain-1.mailguard.com.au.
domain.com mail is handled by 40 filter3.domain-1.mailguard.com.au.
```
* kali@kali:~$ host -t ns domain.com
```
domain.com name server ns1.eisdmn.net.au.
domain.com name server ns2.eisdmn.net.au.
domain.com name server ns3.eisdmn.net.au.
```
* kali@kali:~$ host -t mx domain.com
```
domain.com mail is handled by 20 filter1.domain-1.mailguard.com.au.
domain.com mail is handled by 30 filter2.domain-1.mailguard.com.au.
domain.com mail is handled by 40 filter3.domain-1.mailguard.com.au.
```
* kali@kali:~$ host -t axfr domain.com ns2.eisdmn.net.au
```
Trying "domain.com.au"
Using domain server:
Name: ns2.eisdmn.net.au
Address: 2.3.4.5#53
Aliases: 
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 49685
;; flags: qr aa; QUERY: 1, ANSWER: 63, AUTHORITY: 0, ADDITIONAL: 0
;; QUESTION SECTION:
;domain.com.		IN	AXFR

;; ANSWER SECTION:

All sub domains and their DNS records will appear here
DNS Records: A, AA, CNAME, MX, NS, SOA, SRV, TXT, 
```
* kali@kali:~$ host -l domain.com ns2.eisdmn.net.au
> A and NS records will be displayed in human readable format
```
Using domain server:
Name: ns2.eisdmn.net.au
Address: 2.3.4.5#53
Aliases: 

domain.com name server ns2.eisdmn.net.au.
domain.com has address 1.2.3.4
dns.domain.com has address 3.4.5.6
email.domain.com name server ns1.exacttarget.com.
```
