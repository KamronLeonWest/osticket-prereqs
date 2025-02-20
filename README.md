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

<h2>List of Prerequisite</h2>

- Create a Windows 10 Azure Virtual Machine with 4 vCPUs (create a memorable username and password)
- Download [osTicket Installation Files]([url](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)) within the Virtual Machine

<h2>Installation Steps</h2>

<p>
<img src="https://imgur.com/8tferpX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/lu64B2H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/5gO6FJ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/ysKLJkP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/wunRiUD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/uSKCIyi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/V1lMMEU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/JzSzVMi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the Windows start menu, search and open the control panel. Click Programs, Programs and Features, then 'Turn Windows Features on or off.' Enable internet information services and from there, expand that folder, World Wide Web Services, Application Development Features, and enable CGI. Install PHPManagerForIIS_V1.5.0.msi and rewrite_amd64_en-US.msi from the osTicket Installation files within the virtual machine, then create the file directory C:\PHP. Unzip php-7.3.8-nts-Win32-VC15-x86.zip into the C:\PHP folder, install VC_redist.x86.exe and MySQL 5.5.62 from the osTicket installation files and set the username and password to 'root.'
</p>
<br />

<p>
<img src="https://imgur.com/Gz4DeW1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/taSZpIc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/32LAmm6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/rLTx2De.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/ZK0Zii6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/IAiiIe3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/A3PgQlV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/Y448wFU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin and register PHP from within the IIS. Stop and start the IIS then using the files within the osTicket Installation folder, unzip osTicket-v1.15.8.zip and copy the upload folder into c:\inetpub\wwwroot. Within c:\inetpub\wwwroot, rename upload to osTicket. Start and stop the IIS again, then navigate to Browse 80 from sites, default, and to osTicket.
</p>
<br />

<p>
<img src="https://imgur.com/4IxLXJw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/wK8aDY8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/7iXgmmi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/m8wixDy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To enable the disabled extensions, go back to IIS, sites, Default, and osTicket. Go to PHP Manager, click 'Enable or disable an extension, then enable php_imap.dll, php_intl.dll, and php_opcache.dll. Refresh the osTicket on the browser and observe the changes. Go back to File Explorer and rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php. Right-click ost-config.php into properties, and go to advanced security. Disable inheritance, then create new permissions for everyone. Install HeidiSQL from the osTicket installation folder, create a new session with root as the username and password, connect to session, and create a database called 'osTicket.' Finish setting up osTicket within the browser and set MySQL Database: osTicket, MySQL Username: root, MySQL Password: root, all the other information is dependant on the user. Once you click 'Install Now!' you'd have successfully set up osTicket!

</p>
<br />
