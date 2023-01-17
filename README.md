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
