<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services and Common HTTP Features
- IIS Management Console
- PHP
- HeidiSQL
- OS Ticket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/jnSgnTs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, go to Azure and create your virtual machine. Once created, use Remote Desktop to connect to the VM. Next, open the Start menu and search for 'Windows Features.' Enable Internet Information Services (IIS), CGI, and Common HTTP Features, then click 'OK. 
</p>
<br />

<p>
<img src="https://i.imgur.com/W8pSnb9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, download and install PHP Manager for IIS, the Rewrite Module, VC_redist, and PHP. When installing PHP, extract all files to C:\PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/ge0HeaO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install MySQL and launch it after the installation is complete. Proceed with the standard setup and click 'Execute' to finalize the configuration.
</p>
<br />

<p>
<img src="https://i.imgur.com/lfKqHqz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Start menu, launch Internet Information Services (IIS) Manager as an administrator. Navigate to PHP Manager, and then register a new PHP version by selecting the executable you previously installed and Restart IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/qr46nO5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download osTicket, extract the 'upload' folder into inetpub\wwwroot, and rename it to 'osTicket,' so the path reads inetpub\wwwroot\osTicket. Restart IIS, then navigate to the osTicket folder in IIS Manager. From there, click 'Browse *:80' on the right-hand side.
</p>
<br />

<p>
<img src="https://i.imgur.com/uiAJIjV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We'll need to install some missing extensions. Open PHP Manager in osTicket and enable php_opcache, php_intl, and php_imap.
</p>
<br />

<p>
<img src="https://i.imgur.com/FmkzwM1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename the ost-sampleconfig.php file located in wwwroot\osTicket\include to ost-config.php. Continue your setup of osTicket in the Browser then download and install HeidiSQL
</p>
<br />

<p>
<img src="https://i.imgur.com/4faAFfG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With SQL open, click 'New' to create a new connection by logging in. Right-click 'Unnamed' and select 'Create a New Database,' then name it 'osTicket.'
</p>
<br />

<p>
<img src="https://i.imgur.com/n2GZ9Uc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Complete the setup in the osTicket browser interface, then click 'Install Now' to finish the installation. You're all set!
</p>
<br />
