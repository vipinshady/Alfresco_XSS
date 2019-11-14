# Alfresco Stored XSS Vulnerability

Blind Stored XSS in Alfresco Enterprise 5.2.4

Description:

Alfresco allows users to upload documents which are being save in alfresco portal, an attacker can upload a .html with malicious JavaScript which then executes on the Alfresco portal. During the assessment we were able to execute blind stored cross-site scripting on the Alfresco portal which contains sensitive documents. 

Risk:

A remote attacker can steal victim’s credentials by sending a keylogger JavaScript. Also phishing attacks can be performed by changing the content in .html file which is being executed in the browser. This allows an attacker to perform any action in Alfresco as the logged in user. Additionally, the following attack scenarios are possible:
•	By showing a new login screen the user’s credentials can be hijacked.
•	By adding JavaScript an attacker can redirect a victim to malicious websites.
