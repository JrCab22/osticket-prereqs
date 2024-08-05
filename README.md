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
  
  **Shown below are how you can create a new Resource group and VM. Disregard the errors since these are the ones I already made under the same name.**
  
![image](https://github.com/user-attachments/assets/69f01b82-73ec-455d-9691-947b7a2d22a4)

**Click create once validated**
![image](https://github.com/user-attachments/assets/637c78b8-b993-44d4-9c5c-fe77c7ec57af)



![image](https://github.com/user-attachments/assets/2e90bce5-803a-4d1a-a367-0309ef5b730f)



  - **Allow a new Virtual Network (Vnet) to be created for the VM in the networking section.**

2) Remote into the Windows virtual machine using Microsoft Remote Desktop (Mac) or Remote Desktop (Windows).

3) Locate IIS. (Right click start, click Run, type in control, Go to programs and then to turn Windows on or off). In Windows features, check the box that says Internet Information Services.

   ![image](https://github.com/user-attachments/assets/99db8bbf-a576-440e-9268-65b1c7d0f903)

   ![image](https://github.com/user-attachments/assets/c5e663ac-47ec-4af1-bebd-5f9e6fe90996)


5) To make sure IIS is enabled go to web browser and type 127.0.0.1
   
   ![image](https://github.com/user-attachments/assets/3ab2bba5-f90a-4ae9-b1dd-acf44d9b2b49)

6) Download and Install all the following files: **PHP Manager, Rewrite Module, PHP 7.3.8, VC_redist.x86.exe.,  MySQL 5.5.62, and Heidi SQL. ** 
 
6) Open IIS as an administrator and register PHP

7) Download osTicket version 1.15.38 then move the upload folder to c:\inetpub\wwwroot. Rename upload to osTicket

8) Reload IIS by clicking restart on the Actions side bar.
   
   ![image](https://github.com/user-attachments/assets/fbbf4c93-874c-4365-bffd-20022d58fb5a)

   
10) While in IIS go to sites --> default --> osTicket
   -Click browse 80 on the sidebar to open osTicket Installer
![Screenshot 2024-07-24 164508](https://github.com/user-attachments/assets/ac6559f0-e091-431d-8fbc-dfaef428a4bd)

11) Go back to IIS and enable the following extensions in PHP manager: php_imap.dll, php_intl.dll, php_opcache.dll Refresh the browser.
  ![image](https://github.com/user-attachments/assets/7b297a1c-5ecc-46e1-af51-dcc49c1addca)

 12) Rename: ost-sampleconfig.php to ost-config.php in file explorer.
     -  Go to file explorer --> OsTicket folder --> Include folder --> find ost-sample.config
    
13) Assign Permissions: ost-config.php
      - Disable inheritance -> Remove All
      - New Permissions -> Everyone -> All

14) Continue Setting up osTicket in the browser (click Continue)
    - Name Helpdesk
    - Default email (receives email from customers)

15) Download and install Heidi SQL then open and do the following:
    - Create a new session
    - Connect to the session
    - Create a database name osTicket
   
  16) Finish osTicket setup in the browser assigning a username and password to database.

  17) Click install now!








