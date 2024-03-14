# CVE

### Broken Authorization on change password functionality
**Product**: SmartVista ACS
**Verion**: 2.2.25

**Description**: User can change his password without enter old pass by deleting old password parameters from the request before sending it to the server.

**Steps to reproduce**:
1. Login to the application
2. Request for change password & fill the parameters with new password
3. Send the request to burp proxy

![image](https://github.com/i-Samir/CVE/assets/155354553/42395f9f-204f-4b0a-933a-a2e7bc2b3d2e)

4. Remove the old password parameter before sending the request to server

![image](https://github.com/i-Samir/CVE/assets/155354553/7b9683ef-e259-404b-b840-d0b6525d908d)

5. Password changed successfully without old one 
