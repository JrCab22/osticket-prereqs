# How to install osTicket ticketing system for Windows and Mac
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>Video Demonstration</h1>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial we will be going over a step by step guided walkthrough on how to setup the oS ticketing system on your device. <br />


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
   

**Make sure all the following are checked before installing IIS webserver**:
- Everything under Common HTTP Features
- CGI under Application Development Features
- IIS Manager under Web Management tools


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

 13) Rename: ost-sampleconfig.php to ost-config.php in file explorer.
     -  Go to file explorer --> Windows C drive --> inetpu --> OsTicket folder --> Find the **Include** folder --> find ost-sample.config and rename
     
![image](https://github.com/user-attachments/assets/2c1f4d6f-41e4-46dd-b61d-1feb613cab34)

  
14) Assign Permissions: Right click ost-config.php and go to properties the security. Click the advanced button
      - Click Disable inheritance -> Remove All inherited permissions from this object
      - Click Add --> Select a principal 
      - Type Everyone (just for this practice) -> Click check names
      - Check all the boxes to give everyone full control then click ok
      - Click Apply then ok
    
![image](https://github.com/user-attachments/assets/55c1dbcf-690e-4c08-bcec-118207d8e08a)

![image](https://github.com/user-attachments/assets/fa747b13-9f28-4d53-a38f-491634fb88fe)

![image](https://github.com/user-attachments/assets/ed4d7c1b-d96a-45dd-ae4f-f2da7edd80ba)


15) Continue Setting up osTicket in the browser (click Continue)
    - Enter a name under Helpdesk name and create a default email (receives email from customers).
    - Enter information for primary admin account
    - Make sure to save all the entered information in case!

![image](https://github.com/user-attachments/assets/936b3062-13da-4a38-9d79-f370a57f3fbe)

![image](https://github.com/user-attachments/assets/c5509c82-e8ad-4af7-928f-7c2ec0a9ec0a)


16) Install and open Heidi SQL and do the following:
    - Create a new session (in this we enter instance root, password1)
    - Connect to the session (click open)
    - Create a database name osTicket by right clicking unamed
      
![image](https://github.com/user-attachments/assets/4f534b9a-f213-4a61-ad28-9542b465f483)


   ![image](https://github.com/user-attachments/assets/a1610ac9-3447-4716-8ee5-7fa13f364c2e)


  17) Finish osTicket setup in the browser assigning a username and password to the database.

![image](https://github.com/user-attachments/assets/57545c61-bc0a-4eea-b54e-63770726e37d)

  18) Click install now. Congrats! You have successfully installed the osTicket ticketing system.

![image](https://github.com/user-attachments/assets/b7684a57-151c-4fa3-acb0-c42291c9a6e1)


**Clean up steps:**
1) Delete setup folder in inetpub
2) Change ostconfig to Read only






