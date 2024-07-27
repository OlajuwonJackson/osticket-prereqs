# osticket-prereqs<p align="center">
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

- IIS
- PHP Manager
- VC_redistx86
- MySQL 5.5.62
- Rewrite Module
- Heidi SQL

<h2>Installation Steps</h2>

<p>
</p>
<p>
<h3>&#9312; Create a Virtual Machine on Azure</h3>
The first step to do is to create a virtual machine on Azure. 
Choose the image or base operating system as Windows 10 Pro, version 22H2.</p>
<p>

![image](https://github.com/user-attachments/assets/310160fc-489d-4767-ae9e-068d6cefd28d)


<p>
</p>
<p>
<strong> NOTE: Make sure to set the size to at least 2 vcpus and 16 GiB memory. 
And make sure that RDP (3389) is allowed in "Select inbound ports" in order to permit Remote Desktop access to the VM.</strong> </p>
<p>


![image](https://github.com/user-attachments/assets/e6749a2a-07f3-4b24-b8f3-a8782c1f7eaa)



</p>
<br />

<p>
</p>
<p>
<h3>&#9313; Review and Create </h3>
<p>Click on the last check box to make sure an eligible Windows 10 license is had. Then continue to "Review + create". A validation process will happen. Then once the validation is successfully accomplished and is a pass, proceed to create.</p>

</p>
<br>
<h3>&#9314; Find your VM's public IP address</h3>
<p></p>Permit some time for the deployment to complete then find the VM's public IP address and copy it.</p>
<p>
<img src="https://i.imgur.com/GcAaRUJ.png"
/img>





</p>
<p>
<h3>&#9315; Connect to the VM using the Remote Desktop Connection program</h3>
<p>Open your Remote Desktop Connection program and paste the VM's IP and login with the same login credentials used to create the VM.</p>
<p>
<img src="https://i.imgur.com/mmFqBfd.png"/img>




</p>
<br />
<h3>&#9316; Enable IIS </h3>
<p> Once the VM is open, the next step is to install / enable IIS. For that, the Control Panel needs to be accessed and the programs applet opened. Under programs, "Turn Windows features on or off" needs to be selected.</p>
<p> <img src="https://i.imgur.com/Z1dsODe.png"/img>



  
</p>
<p>Then, enable and expand the following features:</p>
<p> <img src="https://i.imgur.com/nf4iEJN.png"/img>


</p>

<p> [X] Internet Information Services</p>
<p>[X] Web Management Tools </p>
<p>[X] IIS Management Console </p>
<p>[X] World Wide Web Services  </p>
<p>[X] Application Development Features </p>
<p>[X] CGI</p>
<p>[X] Common HTTP Features</p>
<br>
<p> Click okay and the features should be enabled.</p>
<br>
<p> <strong> NOTE: To quickly verify whether the changes were successfully configured, simply type 127.0.0.1 on a browser and the page below should appear. </strong></p>
<img src="https://i.imgur.com/p39TXDd.png"/img>

<br> <br>
<h3>&#9317; Download and Install PHP Manager</h3>
<p> To download and install PHP manager, you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>(PHPManagerForIIS_V1.5.0.msi) 
</p> <br>
<p> <img src="https://i.imgur.com/oWcrOOY.png"/img>


</p> 
<br>
<h3>&#9318; Download and Install the Rewrite Module</h3>
<p>To download and install the rewrite module (rewrite_amd64_en-US.msi), you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> </p>
<p><img src="https://i.imgur.com/Ctrc89D.png"/img>
</p>

</p>
<h3>&#9319; Create a new directory</h3>
<p>Continue to File Explorer and create the directory C:\PHP </p>
<img src="https://i.imgur.com/8XE4JL8.png">

<br>
<br>
<h3>&#9320; Download and install php-7.3.8-nts-Win32-VC15-x86.zip </h3>
<p> Download and install php-7.3.8-nts-Win32-VC15-x86.zip, you can be accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> and unzipping the contents into the newly created folder located at C:\PHP </p>
<img src="https://i.imgur.com/BLQ8jK4.png"/img>

<br>
<h3>&#9321; Download and install VC_redist.x86.exe </h3>
<br>
<h3>&#9322; Download and install MySQL 5.5.62 </h3>
<p> To download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi), you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>  and configure in accordance to the following; </p>
<p> [X] Typical Setup</p>
<p>[X] Launch Configuration Wizard after install </p>
<p>[X]Standard Configuration 
</p>
<br>
<img src="https://i.imgur.com/XuVgB0B.png">

<br>
<h3>&#9323; Launch IIS as an administrator</h3>
<p> Search for IIS in the Windows search bar and right click it and choose open as Administrator</p>
<br>
<h3>&#9324; Register PHP Manager </h3>
<br>
<img src="https://i.imgur.com/c5xzsid.png">


<br>
<br>
<p><strong> NOTE: Registration will require you to provide a path to "php-cgie.exe". Direct it to the PHP folder created before and you will locate the file that is being asked for. 
</strong></p>
<br>
<img src="https://i.imgur.com/9ULyXLs.png">

<br>
<p>
</p> 
<h3>&#9325; Restart the IIS server</h3>
<p> The restart button can be found on the right side of the window.</p>
<br>
<img src="https://i.imgur.com/PvqgL28.png">

<br>
<br>
<h3>&#9326; Download and install osTicket</h3>
<p> Download and install osTicket v1.15.8 from the installation files and extract the contents to c:\inetpub\wwwroot </p>
<br>
<img  src="https://i.imgur.com/3khSfCq.png">

<p> Inside c:\inetpub\wwwroot, Rename “upload” to “osTicket”</p>
<br>
<br>
<h3>&#9327; Restart the IIS server again.</h3>
<img src="https://i.imgur.com/3aRoPMm.png">

<br>
<br>
<h3>&#9328; Launch osTicket </h3>
<p>On the left hand side of IIS, Expand on the VM name -> Sites - > Default Website -> osTicket </p>
<img src="https://i.imgur.com/ujUrojd.png">

<p></p>
<p><strong>NOTE: Make sure to click on osTicket</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<h3>&#9329; Click on Browse *80 to launch osTicket</h3>
<p> On the right side of the window, click on browse *80 </p>
<img src="https://i.imgur.com/QAJf0Jr.png">

<br>
<br>
<br>
<p><strong>This should the cause the browser to open osTicket</strong>.</p>
<br>
<br>
<img  src="https://i.imgur.com/cIVZmDJ.png">

<br>
<br>
<br>
<h3>&#9330; Enable extensions</h3>
<p>Open IIS and click on PHP Manager and select "enable or disable extension". </p>
<p>Enable the following extensions:</p>
<p>[X]Enable: php_imap.dll</p>
<p>[X]Enable: php_intl.dll</p>
<p>[X]Enable: php_opcache.dll</p>
<img  src="https://i.imgur.com/OroIyeG.png">

<br>
<br>
<br>
<h3>&#9331; Refresh osTicket</h3>

<p>Refresh the osTicket page on the browser and notice some extensions will now appear active.</p>
<img  src="https://i.imgur.com/DgHxKWY.png">

<br>
<br>
<br>

<h3>&#12881; Rename ost-config.ph</h3>

<p> Under C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, rename "ost-sampleconfig.ph" to "ost-config.ph"</p>
<img src="https://i.imgur.com/iCFUmrl.png">

<br>
<br>
<br>

<h3>&#12882; Configure ost-config.ph permissions</h3>

<p>Configure ost-config.php permissions by right-clicking and choosing</p>
<p>Properties -> Security -> Advance -> Disable inheritance</p> 
<p>Choose remove all inherited permissions and add everyone as a principal. Choose all boxes to make sure all permissions are given. </p>
<img src="https://i.imgur.com/tecv2I8.png">

<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12883; Proceed with the osTicket installation</h3>

<p> Proceed with the osTicket installer on your browser by completing the first half of the page.</p>
<img src="https://i.imgur.com/dIrLqnK.png">

<br>
<br>
<p><strong>NOTE: Concern should not be had about the database credentials. Those will be filled at a later time.</strong> </p>
<br>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12884; Download and install Heidi SQL from the installation files</h3>

<p>Open Heidi SQL and create a new session. Be certain to fill in the username as root and create a password. After inputting credentials, click open and a new session should appear.
</p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12885; Create new database </h3>

<p>On the left side of the window, right click on "Unnamed" and click create new database and name it "osTicket".</p>
<img  src="https://i.imgur.com/3OWtqkH.png">

<br>
<br>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12886; Complete the signing up process</h3>

<p>Return to the osTicket browser and complete the missing credentials. 
It should look something like this.</p>
<img src="https://i.imgur.com/y0xJKyr.png">


<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12887; Complete the osTicket installation</h3>

<p>Click install and osTicket should begin setting up. </p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h2> Final cleanup steps</h2>
<p>[X] Delete "setup" file located at C:\inetpub\wwwroot\osTicket\setup</p>
<p>[X] Set permissions of "ost-config.php" to read only.</p>
<p> File is located at C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<br>
<br>
<h1> osTicket has been successfully installed!</h1>
