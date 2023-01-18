# osticket-prereqs
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

- Resource Group in Azure
- Windows 10 Virtual Machine in Azure
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/usZ0DCk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once a Windows 10 virtual machine has been created in Azure, log in with RDP. Once logged in, right click the start button and select "run". After selecting "run" type "control panel". Enter the Control Panel and select "Programs". 
</p>
<br />

<p>
<img src="https://i.imgur.com/yCD2Cqd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, select "Turn windows features on or off" and look for "Internet Information Services". Turn on "FTP Server", "Web Management Tools", and"World Wide Web Services". Expand "World Wide Web Services" and turn on "CGI". Select "Ok".
</p>
<br />
<p>
<img src="https://i.imgur.com/yIfYFHL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once CGI has been enabled, open click this link for access to the installation files. https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
  
  From the Istallation files, download and install PHPManagerForIIS_V1.5.0msi and then rewwrite_amd_64_en-US.msi
  
</p>
<br />
<p>
<img src="https://i.imgur.com/rH8fzDg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
  Next, create the directory C:PHP. From the installation files, download PHP 7.3.8 and unzip the contents into C:\PHP.
 </p>
 <br />
 <p>
  <img src="https://i.imgur.com/xi9OxyC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  From the installation files download and install VC_redist.x86.exe. after, download and install MySQL 5.5.62. when installing MySQL, 
  Select "Typical Setup", "Launch Configuration Wizard (after Install)", and "Standard Configuration"
 </p>
 <br />
  <p>
  <img src="https://i.imgur.com/pCr1FQT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
   <br />
   <p>
  Next, open IIS (Internet Information Services Manager) as an admin.
   </p>
   <br />
   <p>
 <img src="https://i.imgur.com/Pjg5vD0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  Register PHP from within IIS and then reload IIS.
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/yULUpiz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  Install osTicket V1.15.8 from the installation files. Next extract and copy "Upload" folder to C:\inetpub\wwwroot. Within C:\inetpub\wwwroot, rename "upload" to "osTicket". After, reload IIS.
</p>
<br />
<p>
  <img src="https://i.imgur.com/SJeIxpx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 </p>
 <br />
 <p>
  In IIS go to Sites->Default->osTicket. On the right, click "Browse*:80". If everything has been done correctly osTicket will open in a new tab.
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/SQAioTe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  Note that some extentions are not enabled.
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/SJeIxpx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  Go back to IIS, Sites->Default->osTicket. Double-click PHP Manager. Click "Enable or disable and extention".
  Enable:
  - php_imap.dll
  - php_intl.dll
  - php_opcache.dll
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/SJeIxpx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   </p>
  <br />
  <p>
  Refresh the osTicket site in your browse, observe the changes.
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/PsTtf1o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  Next, rename file C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\wwwroot\osTicket\include\ost-config.php
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/hRGuRjI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  Next, to the file we recently renamed to "ost-config.php", go to advanced security settings and disable inheritance. Then, create new permissions to give full access to everyone.
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/p9YkYZP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
Next, from the installation files, install Heidi SQL. Then create a new session with a username and password. (I used root/Password1) Connect to the session and create a new database called "osTicket".
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/jnc1zfb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  Next, start setting up osTicket in the browser. Name the helpdesk, input emails and information. (does not need to be valid) 
  MySQL Databse: osTicket
  MySQL Username: root
  MySQL Password: Password1
  Click "Install Now!"
  Congratulations, hopefully it installed with no errors!
  - Browse to your helpn desk login page: http://localhost/osTicket/scp/login.php
  -end user osTicket URL: http://localhost/osTicket/
  </p>
  <br />
  <p>
  <img src="https://i.imgur.com/ICggZzx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  </p>
  <br />
  <p>
  Clean up
  - Delete: C:\inetpub\wwwroot\osTicket\setup
  - Set permissions to "read and execute" only C:\inetpub\wwwroot\osTicket\include\ost-config.php  
  
  
  
