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


 =Install Internet Information Services
 =Install Web Platform Installer
 =Install osTicket
 =Install HeidiSQL

<h2>Installation Steps</h2>

- Step 1: Create your virutal machine in Azure.(Open the installation files to install what is needed) 
- Step 2: Install/Enable IIS in Windows CGI
- Step 3: Download and install the PHP Manager for IIS
- Step 4: Download and install the Rewite Module 
- Step 5: Create the directory C:\PHP
- Step 6: Download and install PHP 7.3.8
- Step 7: Download and install VC_redist.x86.exe
- Step 8: Download and install MySQL 5.5.62
- Step 9: Open IIS as Admin
- Step 10: Register PHP from within IIS
- Step 11: Reload (Open IIS, Stop and Start the Server)
- Step 12: Install osTicket v1.15.8
- Step 13: Reload IIS (open IIS, Stop and Start Server)
- Step 14: Go to sites -> Default->osTicket (Browse .80) 
- Step 15: Enable extensions (Enable php_imap.dII, php_intl.dII, php_opcache.dII) Refresh when done
- Step 16: Rename ost-config.php (From C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to  C:\inetpub\wwwroot\osTicket\include\ost-config.php)
- Step 17: Assign Permissions ost-config.php (Disable inheritance--> Remove ALL, New Permissions--> Everyone--> ALL)
- Step 18: Continue (Name Helpdesk/ default email) 
- Step 19: Download and Install HeidSQL, new session root/Password1 --> Create  a  database called osTickets 
- Step 20: Continue setting up osTicket in the browser 
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!
Congratualtions! 
We will go over post installation setup in our next tutorial. 
*INCLUDE LINK TO NEXT TUTORIAL* 
CLEAN UP! Delete your resources to save Azure credit. 


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
