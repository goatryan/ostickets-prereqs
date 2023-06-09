# ostickets-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. osTicket is an open source help desk management solution that offers ticket management and IT assest management within a suite. The  system can only be deplyed in the cloud and is suited for small and midsize enterprise customers. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create VM in Azure
- <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files</a> 
<h2>Installation Steps</h2>
<h2> Step1: Create Virtual Machine on Azure</h2>

If you  do not know how to create a virtual machine in Azure, look at my tutorial here.
Create a Resource Group. Next create a windows 10 Virtual Machine with 4 Virtual CPUs. Lastly, allow it to create a Virtual Network (Vnet)

Once created log in by using Microsoft Remote Desktop. 

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<p>
  <h2>Step2: Installation</h2>

 We must first install IIS in Windows. We can do this by opening "Control Panel" and clicking Uninstall a program. Then "Turn Window Features on or off" and check the IIS box. Proceed by clicking on Web Management tools and World Wide Web Services. Proceed by extending  "Application Development Features" and finally click on [x]CGI to enable services

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 
Test your web servers by opening up a new browser and typing 127.0.0.1 (loopback/local host). You should see IIS page popup, if not double check and restart procedure.
  
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>

<p>
 From the installation files above download and install the following 
  
  - PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
  - Rewrite Module (rewrite_amd64_en-US.msi) 
- Create the directory C:\PHP
 - PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip)  and unzip contents into C:\PHP
 - VC_redist.x86.exe
 - MySQL 5.5.62 (mysql-5.5.62-win32.msi) 
  - Typical Setup
  - Launch Configuration Wizard (after installing) 
  - Standard Configuration 
  - Use Password1
  
  <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
</p>

<br />
<p>
  Open IIS as an Administrator and Register PHP from within IIS
  Install osTicket v.1.15.8
  - Download osTicket from the Installation Files Folder 
  - Extract and copy the "upload" folder to c:\inetpub\wwwrooot
  - Within c:\inetpub\wwwroot, Rename "upload" to "osTicket"
   
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
 </p>
 
 
 <p>
  Next you can reload IIS (restart) 
  Go to sites-> Default-> osTicket 
  - On the right hand side, click "Browse *:80"
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  </p>


<p>
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes

  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
  </p>


<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
  </p>
  
  <p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
 
 <img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
  </p>
  
  <p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
  </p>
  From the Installation Files, download and install Heidi SQL
  
  - Open HeidiSQL
  -Create a new session 
  -Create database called "osTicket"


<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p>   
  Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

End Users osTicket URL:
http://localhost/osTicket/ 

Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>  

<p>
Notes:
Browse to your help desk login page:
  
  http://localhost/osTicket/scp/login.php  
  
End Users osTicket URL:
  
  http://localhost/osTicket/ 

  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
</p>

 
  
  <br />

