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

<p  align="center">
<img src="https://imgur.com/wJQ7Gs1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a virtual machine. Make sure you select the Windows 10 as the image. The size does not matter, but I recommend and usually use something that has at least 2 vcpus (virtual cpus)
</p>
<br />

<p  align="center">
<img src="https://imgur.com/faH8WNX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
At the bottom of the 'Basics' tab, remember to mark the licensing agreement. All the other settings should be automatically filled so you can proceed to 'Review + Create' the virtual machine.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/SrXwFD4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Log into the virtual machine using the credentials you set earlier, and open the file link listed in the prerequesites above.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/gNlmZK9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once downloaded, right-click to extract all from the folder. Leave the window open because all the files within this folder will need to be frequently accessed for the installation process.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/8tferpX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Navigate to the start menu, and open the 'Control Panel.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/lu64B2H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click Programs
</p>
<br />

<p  align="center">
<img src="https://imgur.com/5gO6FJ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now click 'Turn Windows features on or off.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/3PBNhQV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With the new prompted window open, make sure 'Internet Information Services,' 'Web Management Tools,' and 'World Wide Web Services' are enabled. 
</p>
<br />

<p  align="center">
<img src="https://imgur.com/BQDyKmd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Expand 'World Wide Web Services,' then expand 'Application Developoment Features' and finally, check/enable 'CGI' and click 'OK.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/KIsqnat.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the osTicket installation folder, install 'PHPManagerForIIS_V1.5.0' and 'rewrite_amd64_en-US.' The process is straight forward, so just continue to click next until everything is installed. 
</p>
<br />

<p  align="center">
<img src="https://imgur.com/BXpliyD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Following this, navigate to the 'Windows (C:)' directory to create a new folder
</p>
<br />

<p  align="center">
<img src="https://imgur.com/y8UZ4kZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name the folder PHP
</p>
<br />

<p  align="center">
<img src="https://imgur.com/Lg8RbhW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Return to the osTicket installation folder and right click 'php-7.3.8-nts-Win32-VC15-x86.zip,' then 'Extract All...'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/1z90HRL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set the destination folder to the folder created before in the C: directory.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/ysKLJkP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Return to the osTicket installation folder, install 'VC_redist.x86.exe' and run through the process of installing the 'mysql-5.5.62-win32.msi' file. Set the username and password to 'root' for simplicity, though this can be anything you want it to be. Everything else is straight forward, just go for a standard installation.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/wunRiUD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the Windows start menu, search for 'Internet Information Services' then run the program as an administrator when prompted.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/uSKCIyi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click and open 'PHP Manager.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/V1lMMEU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Register new PHP version' then on the prompted window, navigate to the PHP folder created before and select 'php-cgi.exe.' Conversely, you can just type this in. Reload the IIS by opening IIS and then stopping and starting the server again.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/JzSzVMi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the osTicket installation folder, extract/unzip the 'osTicket-v1.15.8.zip' folder, and copy the 'upload' folder into the directory: c:\inetpub\wwwroot. Within wwwroot, rename 'upload' to 'osTicket.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/Gz4DeW1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Return to the IIS Manager window, then stop and start the server again. Now, under the connections tab on the left of the screen, expand 'Sites,' 'Default Web Site,' and then click osTicket to have it selected. On the right side of the screen, select 'Browse *:80.' This will open osTicket and you will notice a few services have X's next to their names. 
</p>
<br />

<p  align="center">
<img src="https://imgur.com/taSZpIc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable the services highlighted (php_imap.dll, php_intl.dll, php_opcache.dll). Now refresh osTicket and observe the changes.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/32LAmm6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Return to the file explorer window and expand osTicket (previously 'upload' in the wwwroot). Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php. After doing this, right click and select 'Properties.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/rLTx2De.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Under the security tab, select 'Advanced.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/ZK0Zii6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Disable interhitance,' then remove all inherited permissions.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/IAiiIe3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, select 'Add,' and 'Select a principal.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/A3PgQlV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Type in 'everyone,' then click 'Check Names.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/Y448wFU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Select 'Full control' then click 'OK.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/4IxLXJw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, install HeidiSQL from the osTicket installation files. This configuration wizard is simple so once it is installed, open HeidiSQL and create a new session by selecting 'New' at the bottom left part of the prompt menu with the username and password both set to 'root.' Once this is set, select 'Open' then proceed.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/wK8aDY8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Right click the 'Unnamed' session, tab 'Create new,' then select Database.
</p>
<br />

<p  align="center">
<img src="https://imgur.com/7iXgmmi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name this database 'osTicket.'
</p>
<br />

<p  align="center">
<img src="https://imgur.com/m8wixDy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finish setting up osTicket within the browser and set MySQL Database: osTicket, MySQL Username: root, MySQL Password: root, all the other information is dependant on the user. Now, click 'Install Now'
</p>
<br />

<p align="center">
Congradulations! With all this set, you will have successfully set up osTicket!
</p>
