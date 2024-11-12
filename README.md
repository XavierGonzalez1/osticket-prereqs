<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Interner Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MYSQL
- osTicket v1.15.8
  
<h2>Installation Steps</h2>


First thing you want to do is to create a Virtual MAchine (VM) with Windows 10 pro in Azure Portal. 

***Note: Size should have atleast 2 vcpus and 8 GIB of memory.***

![image](https://github.com/user-attachments/assets/64f5f09c-9aeb-4f5a-aebd-faeff4b9382f)
<p>
</p>
<p>
</p>
<br />

  Once the Virtual Machine is created log into the VM with Remote Desktop by using the public IP address given during the set up!

![image](https://github.com/user-attachments/assets/052e9e93-c084-47cc-86a7-3bb09c56a8ae)

![image](https://github.com/user-attachments/assets/2e648d25-d9fc-4171-bcea-26970e6bc873)

<br />
</p>
<p>
Within the VM you then have to enable the Internet Information Services (IIS). To enable IIS open
Control Panel-> Uninstall a Program-> Turn Windows features on/off check ISS box and expand the folder by double clicking to find World Wide Web Services. From here expand the WWW folder and find Application Devellopment Features and expand the folder to check the CGI box and enable it. 
</p>
<p>
  
![image](https://github.com/user-attachments/assets/374e300b-f469-4cd1-a63b-d2768ea5ce63)

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
