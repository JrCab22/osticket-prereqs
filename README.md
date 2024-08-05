# osTicket-Installation
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial we will be going over a step by step guided walkthrough on how to setup the oS ticketing system on your device. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- PHP 7.3.8
- C_redist.x86.exe.
- MySQL 5.5.62
- Heidi SQL

<h2>Installation Walkthrough</h2>


<p>

<p>
1) Create a resource group for OS ticket and a Windows 10 virtual machine assigned to that group in the Microsoft Azure Portal. 
  
  - **Allow a new Virtual Network (Vnet) to be created for the VM in the networking section.**

2) Remote into the Windows virtual machine using Microsoft Remote Desktop (Mac) or Remote Desktop (Windows).

3) Once logged in, locate IIS. (Right click start, click Run, type in control, Go to programs and then to turn Windows on or off). In Windows features, check the box that says Internet Information Services.

   ![image](https://github.com/user-attachments/assets/99db8bbf-a576-440e-9268-65b1c7d0f903)

   ![image](https://github.com/user-attachments/assets/c5e663ac-47ec-4af1-bebd-5f9e6fe90996)
   

**Make sure all the following are checked under Common HTTP features before installing IIS webserver**

![image](https://github.com/user-attachments/assets/0192c0c0-0d40-4e15-908e-2a990e82e09a)


**To make sure IIS is enabled go to web browser and type 127.0.0.1**
   
   ![image](https://github.com/user-attachments/assets/3ab2bba5-f90a-4ae9-b1dd-acf44d9b2b49)

4) Download and Install all the following files: **PHP Manager, Rewrite Module, VC_redist.x86.exe. and MySQL 5.5.62.**

5) Create a new folder in the Windows C Drive called PHP
   
   ![image](https://github.com/user-attachments/assets/c3bf9b65-c6d3-42c1-a775-8c8af1bbc113)

6)  Download and unzip PHP 7.3.8 to the C:\PHP folder

 
![image](https://github.com/user-attachments/assets/bee1315e-6325-455a-8e85-e41193480e88)

 
7) Open IIS as an administrator and register PHP.
    - **IIS --> PHP manager --> Register new PHP version --> Double click php-cgi from PHP folder --> Select ok**
  
   
 ![image](https://github.com/user-attachments/assets/f6983f8c-5ccb-42f5-9577-7bf18eedd71a)

 ![image](https://github.com/user-attachments/assets/59151779-9eb2-423e-9e99-6ce4fe891f6b)

8) Reload IIS by clicking restart on the Actions side bar.
   
   ![image](https://github.com/user-attachments/assets/fbbf4c93-874c-4365-bffd-20022d58fb5a)
   
9) Download osTicket version 1.15.38 then drag the **Upload** folder to c:\inetpub\wwwroot. Rename **Upload** folder to **osTicket**

![image](https://github.com/user-attachments/assets/9faa3bb3-2798-48b7-9ecd-40551ade8ae9)

10) Reload IIS again
   
11) While in IIS go to sites --> default --> osTicket
   -Click browse 80 on the sidebar to open osTicket Installer
![Screenshot 2024-07-24 164508](https://github.com/user-attachments/assets/ac6559f0-e091-431d-8fbc-dfaef428a4bd)

12) Go back to IIS and enable the following extensions in PHP manager: **php_imap.dll, php_intl.dll, php_opcache.dll**. Refresh the browser.

  ![image](https://github.com/user-attachments/assets/31329e37-c86d-443a-a367-70c782019ae0)


  ![image](https://github.com/user-attachments/assets/7b297a1c-5ecc-46e1-af51-dcc49c1addca)

 14) Rename: ost-sampleconfig.php to ost-config.php in file explorer.
     -  Go to file explorer --> OsTicket folder --> Include folder --> find ost-sample.config
    
15) Assign Permissions: ost-config.php
      - Disable inheritance -> Remove All
      - New Permissions -> Everyone -> All

16) Continue Setting up osTicket in the browser (click Continue)
    - Enter Name (Helpdesk)
    - Default email (receives email from customers)

17) Open Heidi SQL and do the following:
    - Create a new session
    - Connect to the session
    - Create a database name osTicket
   
  18) Finish osTicket setup in the browser assigning a username and password to database.

  19) Click install now!








