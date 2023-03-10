# WebApplicationPT
Complete web application penetration testing methodology research.
## Standards used
* OWASP Top 10
* WSTG v4.2,4,3
* WASC 40
* SANS 25
## Checklist
* Login Page Checks
```
Native login:
  > Insufficient anti-automation - CAPTCHA, Re-CAPTCHA
  > Account lockout policy - Bruteforce on the login
  > Default credentials bruteforcing
  > Username/ Email addresspage enumeration
HTTP Basic Authenticaton
NTLMv1 and NTLMv2
SSO (SAML)
OAuth1
OAuth2
Auth0
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
