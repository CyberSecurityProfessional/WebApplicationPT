# WebApplicationPT
Complete web application penetration testing methodology research.
## Purpose of Penetration Testing
To break the system's Authn, Authz, and Confidentiality, Intigrity, Availability (CIA)
## Types of Security Testing
```
Vulnerability Assessment (VA)
  > Only automated scans and false positives
Vulnerability Assessment and Penetration Testing (VAPT)
  > Automated scans and false positives
  > Manual penetration testing (Intrusive testing and interactive exploitation)
```
## Types of penetration testing
* Based on the testing approach
```
White box: Covers both static application security testing (SAST) and dynamic application security testing (DAST)
  > SAST: Source Code Review, Dependency Scan, Software Component Analysis
  > DAST: Automated Scanners, Tools, Manual Penetration Testing
Grey box: Covers only DAST (Application domain name, credentials and application walkthrough will be given)
Black box: Only in-scope application domain name will be given.
  > Approach, tools, intrusive level can be anything and everything is attackers choice.
  > Aim: To break into the system's Authn, Authz, and Confidentiality, intigrity, Availability (CIA) from zero (without having any prior knowledge on the application/ Environment).
```
* Based on the environment
```
Internal PT:
  > Preferred PT: White box
  > Preferred Reviews:
        Over all Application architecture review
        Application Server configuration review
        Web server configuration review (Server hardening)
        Cloud configuration review (SaaS, PaaS, IaaS)
        Database server configuration review
        Docker containers, Kubernetes
        CDN - Cloudflare, Etc.
External PT:
  > Prefered PT: Grey box (or) Black box
```
* Based on the intrusive level
```
Intrusive (Ex: Exploiting OS command injection, SQL injection, SSRF, etc)
Non-intrusive (No exploitation)
```
## Standards used
* OWASP Top 10
* WSTG v4.2,4,3
* WASC 40
* SANS 25
## Initial Steps
* Attend application's walkthrough demo call (or) Watch call record
* Questionnaire
## Checklist
### Information Gathering
* Client documents:
```
> Security Assessment Readiness document (SAR) (or) Factsheet
> Demo call
> Application training videos
> Application documents, User guide and manual
```
* Port enumeration
```
nmap
```
* Automated Web Scanner
```
nikto
```
* Directory listing vulnerability
* Directory Search or Directory bruteforcing
```
1. dirb
2. dirsearch
```
* Sub domain enumeration
```
1. Zone transfers Attack
2. Sub domain enumeration Tools
3. Brute forcing - list of subdomains
```
* Enumerating to identify admin login pages
### Technology based checks
* JavaScript frameworks
```
Angular JS
Node Js
React JS
Electron JS
```
* Server operating system
```
Windows
Linux flavour
```
* Application Server
```
Apache - Tomcat
IIS
Nginx
```
* Programming language used
```
ASP.NET
Java
PHP
```
* Hosting platform
```
Cloud
> AWS
> Azure
> GCP
> Digital Ocean
> Alibaba
On primises
Shared hosting
VPS
```
* Content Delivery Network (CDN)
* Platforms
```
Ruby on Rails (RoR)
```
* Content Management System
```
Wordpress - PHP
Drupal
Joomla
```
### Regular checklist
* Login Page Checks
```
Native login:
  > Insufficient anti-automation - CAPTCHA, Re-CAPTCHA
  > Account lockout policy - Bruteforce on the login
  > Default credentials bruteforcing
  > Username/ Email addresspage enumeration
HTTP Basic Authenticaton
Platform based authentication:
  > NTLMv1
  > NTLMv2
SSO (SAML)
OAuth1.0
OAuth2.0
Auth0
OpenID
```
* Signup/Register/Create account form checks
```
Insufficient anti-automation - CAPTCHA, Re-CAPTCHA
Username/ Email addresspage enumeration
```
* Contact us form
```
Insufficient anti-automation - CAPTCHA, Re-CAPTCHA - Inbox flooding attack
```
* Forgot password operation
```
Insufficient anti-automation - CAPTCHA, Re-CAPTCHA - inbox flooding attack
Host header attack
```
* Request smuggling attack
```
Tool: Request smuggler tool
git clone https://github.com/defparam/smuggler.git
cd smuggler
python3 smuggler.py -u https://sub.domain.com
```
* zone transfers attack
# In progress
