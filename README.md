<h1>Building and Configuring Active Directory (IN PROGRESS)</h1>

<br />
<h2>Description</h2>
Text

<h2>Utilities Used</h2>

- <b>Sever Manager</b> 
- <b>Active Directory Users and Computers</b>

<h2>Environments Used </h2>

- </b>Windows Sever 2022 through Oracle Virtual Box</b>
- </b>Windows 10 Pro</b>

<h2>Lab Overview:</h2>

<p align="center">
Once I the Windows Sever 2022 took its time installing, the first step was to change the name of the Sever/Pc for ease of use. This was done by opening file explorer, right clicking on "This Pc", going to properties, and clicking reanme. I renamed the device to Windowsserver2022Lab. This prompted a restart of the server and upon restart, can confirm the name has been changed.<br/>
<img src="https://github.com/user-attachments/assets/6ff6a1b8-5f1d-494f-9f6d-d4dce962c462" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/fbfbb16a-8cb3-4058-a1fa-d48f11aadfdd" alt="Active Directory Projext"/>
<br />
<br />
Windows Servers come with Server Manager pre-installed which allows you to install and configure other apps and services. The first I thing I configured was Active Directory Domain Services (AD DS). AD DS allows domain controllers is the heart of Active Directory allowing domain controllers to give access to the many services to domain users. Within the AD DS configuration, becasue I am creating a new domain, I added a new forest, and made the root domain "ADLab.local". As the domain, well needed to be a domain like .com, .org, for DNS forward lookups or so connecting between users can use domain names rather than IP addresses.<br/>
<img src="https://github.com/user-attachments/assets/0a7ad493-1d49-404e-9014-520f78dbbcd0" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/e22f6cbf-968f-49c9-b742-186dadb97445" alt="Active Directory Projext"/>
<br />
<br />
Once I finished configuring the wizard, I was prompted with another restart which, upon being presented with the login screen, confirmed the initial success of a new domain by the domain (ADLAB) followed by the user (Administrator).<br/>
<img src="https://github.com/user-attachments/assets/66b47822-159b-4823-b288-5f7ea0055b93" alt="Active Directory Projext"/>
<br />
<br />
I then pivoted to the second most important part of the Active Directory system and that is Active Directory Users and Computers (AD UC). Within AD UC, I opened the domain ADLab.local, right-clicked on Users and created the user "helpdesk" and right clicked on the administrator account and copied it to the helpdesk, giving helpdesk full administrative priviliges that I will use for all tasks that need admin rights in the future.<br/>
<img src="https://github.com/user-attachments/assets/1bea91cb-7b8a-4e0c-bd0e-3c33f71d1fcf" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />
Text<br/>
<img src="" alt="Active Directory Projext"/>
<br />
<br />

<h2>Thoughts</h2>
text
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
