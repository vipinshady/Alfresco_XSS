# Alfresco Stored XSS Vulnerability



Blind Stored XSS in Alfresco Enterprise 5.2.4



Description:



Alfresco allows users to upload documents that are being saved in the alfresco portal, an attacker can upload a .html with malicious JavaScript which then executes on the Alfresco portal. During the assessment, we were able to execute blind stored cross-site scripting on the Alfresco portal which contains sensitive documents.



Risk:



A remote attacker can steal the victim’s credentials by sending a keylogger JavaScript. Also, phishing attacks can be performed by changing the content in the .html file which is being executed in the browser. This allows an attacker to perform any action in Alfresco as the logged-in user. Additionally, the following attack scenarios are possible:

• By showing a new login screen the user’s credentials can be hijacked.

• By adding JavaScript an attacker can redirect a victim to malicious websites.



Below is the POC for the Stored Cross-site scripting:



Malicious HTML file uploaded by a remote attacker in the Alfresco portal:


![Image of Alfresco](https://1.bp.blogspot.com/-tP5c4Hf6y8I/XffgQB7oz0I/AAAAAAAAH5U/JNfNHxGar-EGX8R7B4SYKFYN-9N5uIS-QCLcBGAsYHQ/s1600/Alfresco%2B1%2Bcopy.png)




Cross-site scripting (XSS) is triggered in the Alfresco portal as the victim clicks on "view in browser" tab.


![Image of Alfresco](https://1.bp.blogspot.com/-nBl9bzf7nk8/Xd2e5p7PXHI/AAAAAAAAH3I/I3YPhm8Zb5cnL_DAWihMVJPw7Nz1nsa-gCLcBGAsYHQ/s1600/Alfresco%2B2.png)






Another example of a phishing page by modifying the content in the HTML page.


![Image of Alfresco](https://1.bp.blogspot.com/-ACotGl7TI70/Xd2e5hMqqaI/AAAAAAAAH3Q/PhJ331apIJIEYZ5BJSeZhgtTmlNxxpxcgCLcBGAsYHQ/s1600/Alfresco%2B3.png)






Thank you for reading!
