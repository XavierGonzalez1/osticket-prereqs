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

</p>
<p>

  
Within the VM you then have to enable the Internet Information Services (IIS). To enable IIS open
Control Panel-> Uninstall a Program-> Turn Windows features on/off check ISS box and expand the folder by double clicking to find World Wide Web Services. From here expand the WWW folder and find Application Devellopment Features and expand the folder to check the CGI box and enable it. 


</p>
<p>
  
![image](https://github.com/user-attachments/assets/374e300b-f469-4cd1-a63b-d2768ea5ce63)

</p>
<p>

  
Once IIS is enabled, download and install the PHP Manger (PHPManagerforIIS_V1.5.0.msi) and Rewrite Module (rewrite_amd64_en-US.msi) which both can be found <a href="https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0"> here! 

  
</p>
<p></p>

<img width="1213" alt="Screenshot 2024-11-12 at 3 57 37 PM" src="https://github.com/user-attachments/assets/cc30d07e-5a93-4fb4-a6f5-cebbddcbed35">

<img width="1125" alt="Screenshot 2024-11-12 at 4 08 13 PM" src="https://github.com/user-attachments/assets/072555a9-7999-4df8-ac6c-4531e02df573">

</p>
<br />
</p>


After installing the Rewrite Module create a new folder within the Windows (C:) called PHP. Extract the ***(php-7.3.8-nts-Win32-VC15-x86.zip)*** folder to the New PHP folder in the (C:) drive. Next instal (VC_redist.x86.exe).  


<img width="641" alt="Screenshot 2024-11-12 at 4 20 59 PM" src="https://github.com/user-attachments/assets/749ff71f-b39f-4546-bc69-af4237a9248e">

<img width="642" alt="Screenshot 2024-11-12 at 4 26 14 PM" src="https://github.com/user-attachments/assets/723d17d8-8d8c-4406-8855-9f968ddd2ba6">

<img width="577" alt="Screenshot 2024-11-12 at 4 28 24 PM" src="https://github.com/user-attachments/assets/206e1a35-7bb6-4bc6-b24d-c2f2ad3ce1ec">
</p>
</p>
<br />


Next install the (VC_redist.x86.exe) file first and (MySQL 5.5.62) second. Choose "Typical" setup type and install-> launch MySQL Server and select "Standard Configuration". In the Modify Security Settings the "New root password" needs to be ***root*** for the sake of the lab the username will be ***root*** and password will be ***root***.  
</p>


<img width="470" alt="Screenshot 2024-11-12 at 5 07 22 PM" src="https://github.com/user-attachments/assets/3166c0ee-2d3f-4173-b554-49cc05474453">

<img width="501" alt="Screenshot 2024-11-12 at 5 13 13 PM" src="https://github.com/user-attachments/assets/120cb660-50ce-41f5-b066-8695b7fd79e4">
</p>
<br />
</p>

Before osTicket can be installed we need to open IIS as an admin-> Register PHP Manager-> Browse and select (php-cgi.exe). After registering the PHP CGI file reload the server by stopping and starting it. 


<img width="1061" alt="Screenshot 2024-11-12 at 5 31 03 PM" src="https://github.com/user-attachments/assets/2e52c657-cfe4-47ff-86e3-5391c054c3f7">

<img width="698" alt="Screenshot 2024-11-12 at 5 31 36 PM" src="https://github.com/user-attachments/assets/bb104570-896a-47ee-8594-cd2f03537c93">

<img width="790" alt="Screenshot 2024-11-12 at 5 32 52 PM" src="https://github.com/user-attachments/assets/744c62e9-74ea-43bf-b516-0eca27af7c89">

<img width="1060" alt="Screenshot 2024-11-12 at 5 34 05 PM" src="https://github.com/user-attachments/assets/e050e097-d066-420b-b5c8-fdbb958fe619">

</p>
<br />
</p>


From the installation file extract the osTicket v1.15.8 file and copy the ***"upload"*** folder to Windows(C:)-> Inetpub-> wwwroot and rename it to "osTicket". Once you have renamed the folder open IIS again to stop and start the server. 


<img width="642" alt="Screenshot 2024-11-12 at 5 51 58 PM" src="https://github.com/user-attachments/assets/26f27ff3-5a17-4169-8b9f-c575a7f2a9ae">

<img width="1536" alt="Screenshot 2024-11-12 at 5 55 18 PM" src="https://github.com/user-attachments/assets/529a34be-e16c-48ec-b69a-658dd934f41b">

<img width="789" alt="Screenshot 2024-11-12 at 5 56 00 PM" src="https://github.com/user-attachments/assets/57462a41-cb1a-4861-99a4-246cb7e1d495">


</p>
</p>


Within IIS go to Sites-> Default Web Site-> osTicket and click "Browse *:80" to make sure the osTicket site is running.


<img width="1262" alt="Screenshot 2024-11-12 at 6 04 53 PM" src="https://github.com/user-attachments/assets/4ed5ea67-819b-46ae-b9bc-e0eeb82acba6">

<img width="842" alt="Screenshot 2024-11-12 at 6 10 01 PM" src="https://github.com/user-attachments/assets/5982ac0f-aad3-46ec-971d-71b23453e47e">

</p>
</p>p

In IIS go back into osTicket


















