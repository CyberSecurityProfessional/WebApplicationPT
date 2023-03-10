# WebApplicationPT
Complete web application penetration testing methodology research.
## Purpose of Penetration Testing
To break the system's Authn, Authz, and Confidentiality, Intigrity, Availability (CIA)
## Types of testing
```
Vulnerability Assessment (VA)
  > Only automated scans
Vulnerability Assessment and Penetration Testing (VAPT)
  > Automated scans
  > Manual penetration testing
```
## Types of penetration testing
* Based on the testing approach
```
White box: Covers both static application security testing (SAST) and dynamic application security testing (DAST)
  > SAST: Source Code Review, Dependency Scan, Software Component Analysis
  > DAST: Automated Scanners, Tools, Manual Penetration Testing
Grey box: Covers only DAST (Only application domain name and credentials will be given)
Black box: Only in-scope application domain name will be given.
  > Approach, tools, intrusive level can be anything and everything is attackers choice.
  > Final goal: To break the system's Authn, Authz, and Confidentiality, intigrity, Availability (CIA) from zero (without having any prior knowledge on the application/ Environment).
```
* Based on the environment
```
Internal PT
  > Prefered: White box, Grey box
External PT
  > Prefered: Blackbox
```
* Based on the intrusive level
```
Intrusive
Non-intrusive
```
## Standards used
* OWASP Top 10
* WSTG v4.2,4,3
* WASC 40
* SANS 25
## Checklist
### Information Gathering
```
Client documents:
  > Security Assessment Readiness document (SAR) (or) Factsheet
  > Demo call
```
```
Other checklist here
```
* Sub domain enumeration
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
Platform based authentication
  > NTLMv1
  >NTLMv2
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
