<h1>Installing and Building an Active Directory Domain(IN PROGRESS)</h1>

<br />
<h2>Description</h2>
Text

<h2>Utilities Used</h2>

- <b>Sever Manager</b> 
- <b>Active Directory Users and Computers</b>

<h2>Environments Used </h2>

- </b>Windows Sever 2022</b>
- </b>Windows 10 Pro</b>

<h2>Lab Overview:</h2>

<p align="center">
I begun the project by first downloading an installing Windows Sever 2022 through Virtual Box. Once, it booted up, the first step was to change the name of the Sever/Pc for ease of use. This was done by opening file explorer, right clicking on "This Pc", going to properties, and clicking rename. I renamed the device to Windowsserver2022Lab. This prompted a restart of the server and upon restart, can confirm the name has been changed.<br/>
<img src="https://github.com/user-attachments/assets/6ff6a1b8-5f1d-494f-9f6d-d4dce962c462" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/fbfbb16a-8cb3-4058-a1fa-d48f11aadfdd" alt="Active Directory Projext"/>
<br />
<br />
Windows Servers come with Server Manager pre-installed which allows you to install and configure other apps and services. The first I thing I configured was Active Directory Domain Services (AD DS). AD DS allows domain controllers to provide the essential services to the domain users, it is basically the heart of Active Directory. Within the AD DS configuration, becasue I am creating a new domain, I added a new forest, and made the root domain "ADLab.local". As the domain, well needed to be a domain like .com, .org, for DNS forward lookups, meaning connecting between users can use domain names rather than IP addresses.<br/>
<img src="https://github.com/user-attachments/assets/0a7ad493-1d49-404e-9014-520f78dbbcd0" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/e22f6cbf-968f-49c9-b742-186dadb97445" alt="Active Directory Projext"/>
<br />
<br />
Once I finished configuring the wizard, I was prompted with another restart which, upon being presented with the login screen, confirmed the initial success of a new domain by the domain (ADLAB) followed by the user (Administrator).<br/>
<img src="https://github.com/user-attachments/assets/66b47822-159b-4823-b288-5f7ea0055b93" alt="Active Directory Projext"/>
<br />
<br />
I then pivoted to the second most important part of the Active Directory system and that is Active Directory Users and Computers (AD UC). Within AD UC, I opened the domain ADLab.local, right-clicked on Users and created the user "helpdesk" and right clicked on the administrator account and copied it to the helpdesk, giving helpdesk full administrative privileges that I will use for all tasks that need admin rights in the future.<br/>
<img src="https://github.com/user-attachments/assets/1bea91cb-7b8a-4e0c-bd0e-3c33f71d1fcf" alt="Active Directory Projext"/>
<br />
<br />
On the Windows Server, I statically assigned an IP address, default gateway, subnet mask, and made it the primary DNS resolver. For DNS in the domain to function, the domain controllers need to be the primary DNS Server for the domain users.<br/>
<img src="https://github.com/user-attachments/assets/fc1a5f20-f3b2-4313-81c6-f70120a00a00" alt="Active Directory Projext"/>
<br />
<br />
I then downloaded and configured the first Windows 10 Pro endpoint. Within Computer Management, I enabled the Administrator account and deleted the User account 'test' I made for setting up the machine. Under Programs and Features I installed many Remote Server Administration Tools (RSAT) to manage Active Directory and other domain users. Lastly, I changed the name of the machine to Lab-Desktop-2 and restarted the machine for changes to take affect.<br/>
<img src="https://github.com/user-attachments/assets/b2cbd210-0862-429b-a98d-3b670ea0bd9b" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/29cb2ce0-9689-48fe-9e87-81db81f34b78" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/eec79ddc-5d17-414f-ae5d-2a8935986f6a" alt="Active Directory Projext"/>
<br />
<br />
After the restart, I went to change adapter settings, clicked IPv4 as I did with the server/Domain Controller and statically assigned the nesassary layer 3 addresses for it to become apart of the same 10.1.10.0 network. Within the Virtual Box application on the Windows Server and Widows 10 VM, I changed the network settings to be host-only adapater. I confirmed that they were on the same network by successfully pinging the Windows Server from the Windows 10 endpoint. Lastly, on the Windows 10 machine, I opened System Propeties and joined the ADLab.local domain finalizing the connection between the Sever and Client.<br/>
<img src="https://github.com/user-attachments/assets/1c50f6d6-9a05-4cdc-9b8b-54947db711bf" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/2744ba93-5cd1-4595-80ef-e178263a1542" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/445c3324-b36d-4b6b-8c51-108b97b8eb3e" alt="Active Directory Projext"/>
<br />
<br />
Next, with AD UC I created the user john smith, this will act as standard user where I will test different group policies and Active Directory functions on. I installed another Windows 10 Pro VM for that user to have. On the second Windows 10 client machine, I followed the same steps of changing the Computer's name to Desktop2, statically assigned the layer 3 addresses so it can be a part of the network of the domain and then successfully joined the domain.<br/>
<img src="https://github.com/user-attachments/assets/b2977214-b297-4d4e-bef8-498a56584b35" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/a78f210f-14a8-4c0f-abc0-a3c6b104c935" alt="Active Directory Projext"/>
<img src="https://github.com/user-attachments/assets/fece4b68-a915-46d5-b40d-f6e027e60e2c" alt="Active Directory Projext"/>
 <img src="https://github.com/user-attachments/assets/10f99e0b-987d-41a1-ba98-3f298fc3f617" alt="Active Directory Projext"/>
<br />
<br />
At this point I have installed the Windows Server and Active Directory services, created two user accounts, helpdesk with administrative privileges and john smith who I created the OU HR for and moved him into it. I created two and configured two Windows 10 Pro VMs and connected them to the Domain Contoller succesfully. With the base installation of the Active Direcotry Forest, two client machines, one for administrating the other client john smith, I will move on to configuring and expirementing with different functions and add ons in Active Directory in the next repository.<br/>
<br />
<br />



<h2>Thoughts</h2>
Other than waiting a considerable amount of time for the .isos to download and then for Virtual Box to set them up, I did not run into any roadblocks. I have set up an Active Directory environment prior for a cybersecurity project so I was familiar with the steps here but it was a great refresher. I am excited that now I have a functional Active Directory domain that I can break, fix, and test stuff with.
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
