# sslscan output analysis
```
While scanning the application, we observed that the following domains are vulnerable to different SSL-related issues.

https://auth.as.com - Lucky13 attack
https://api.as.com - Sweet32 attack, Luck13 attack, RC4
https://goapi.as.com - Sweet32, Luck13, RC4
https://push-notification.as.com - Sweet32, Luck13, RC4
https://printerapi.my.com - Sweet32, Luck13, RC4

Disable the following ciphers:
RC4-SHA
RC4-MD5
DES
CBC

We have observed different results in the SSL scans this time. Please check sslscans.html from the attachments.

Observations:
We have observed the following vulnerabilities.
https://www.as.com - Secure Renegotiation, Breach attack
https://auth.as.com - Lucky13 attack
https://auth-ui.as.com - Secure Renegotiation
https://api.as.com - TLSv1.0, TLSv1.1 are enabled and TLSv1.3 is disabled, not supported TLS Fallback SCSV, Sweet32, Beast, Lucky13, RC4
https://goapi.as.com - TLSv1.0, TLSv1.1 are enabled and TLSv1.3 is disabled, not supported TLS Fallback SCSV, Sweet32, Beast, Lucky13, RC4
https://push-notification.as.com - TLSv1.0, TLSv1.1 are enabled and TLSv1.3 is disabled, not supported TLS Fallback SCSV, Sweet32, Beast, Lucky13, RC4
https://printerapi.my.com - TLSv1.0, TLSv1.1 are enabled and TLSv1.3 is disabled, not supported TLS Fallback SCSV, Sweet32, Beast, Lucky13, RC4

Remediations:
https://www.as.com:
Support "Secure Renegotiation"
Disable HTTP compression.
https://auth.as.com:
Disable AES128 and AES256
https://auth-ui.as.com:
Support "Secure Renegotiation"
https://api.as.com & https://goapi.as.com & https://push-notification.as.com & https://printerapi.my.com:
Disable TLSv1.0 and TLSv1.1
EnableTLSv1.3
support TLS Fallback SCSV
Disable RC4-SHA RC4-MD5 ciphers.
Disable AES128 and AES256 ciphers.
Disable 3DES ciphers.
```
