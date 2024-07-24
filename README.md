# osticket-prereqs
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

- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- PHP 7.3.8
- C_redist.x86.exe.
- MySQL 5.5.62
- Heidi SQL

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/3ab2bba5-f90a-4ae9-b1dd-acf44d9b2b49)


<p>

<p>
1) Create a resource group for OS ticket and a virtual machine in the Microsoft Azure Portal.
  
2) Remote into the virtual machine and locate IIS. (Right click start, click Run, type in control, Go to programs and then to turn Windows on or off). In Windows features, check the box that says Internet Information Services.
   
3) To make sure IIS is enabled go to web browser and type 127.0.0.1
4) Download and Install all the following files: PHP Manager, Rewrite Module, PHP 7.3.8, VC_redist.x86.exe.,  MySQL 5.5.62, and Heidi SQL.  
  - PHP 7.3.8 to C:\PHP folder (newly created directory)
5) Open IIS as an admin and register PHP
6) Download osTicket from the Installation files folder then move the upload folder to c:\inetpub\wwwroot. Rename upload to osTicket

7) Reload IIS by clicking restart on the side bar.
8) While in IIS go to sites --> default --> osTicket
   -Click browse 80 on the sidebar
![Screenshot 2024-07-24 164508](https://github.com/user-attachments/assets/ac6559f0-e091-431d-8fbc-dfaef428a4bd)

9) Enable the following extensions: php_imap.dll, php_intl.dll, php_opcache.dll. Refresh the browser.
10) 


