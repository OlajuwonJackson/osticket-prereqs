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

<img width="758" alt="2" src="https://imgur.com/a/AfJun7w">

<p>
</p>
<p>
<strong> NOTE: Make sure to set the size to at least 2 vcpus and 16 GiB memory. 
And make sure that RDP (3389) is allowed in "Select inbound ports" in order to permit Remote Desktop access to the VM.</strong> </p>
<p>

<img width="757" alt="3" src="https://private-user-images.githubusercontent.com/163789590/313890077-82b2c67a-3b78-43c8-8980-8725923375ad.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwMDc3LTgyYjJjNjdhLTNiNzgtNDNjOC04OTgwLTg3MjU5MjMzNzVhZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03YjQ4NDIyZGZmMTE2Mjg4MDc2YzY5YjRlZjBlNzI2ZDdhNTc2M2VlYWMwYjFkY2JmOTMyNzgzOTNkNDdiMWE1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.bCTKUNG-P8p4EleBvci5uHC8kX6lMbdzk3REJRW9QUM">



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
<img width="1009" alt="4" src="https://private-user-images.githubusercontent.com/163789590/313890216-941a738c-e208-4aac-a182-acfcec531367.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwMjE2LTk0MWE3MzhjLWUyMDgtNGFhYy1hMTgyLWFjZmNlYzUzMTM2Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00MzNjM2M5MTQxOTQ5MjkzNjg3NmI1N2RmMzVjOGU4MzRjMWRkM2ZlNzNhOTk5MTg3OTY3NDc4NDhjYTBlM2FjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.HhHqBlrXQm7bw3q7gVZymBcXgZaabHiyXQmOkeuTT4U">



</p>
<p>
<h3>&#9315; Connect to the VM using the Remote Desktop Connection program</h3>
<p>Open your Remote Desktop Connection program and paste the VM's IP and login with the same login credentials used to create the VM.</p>
<p>
<img width="302" alt="5" src="https://private-user-images.githubusercontent.com/163789590/313890246-f285eec1-0d5c-4246-bd4f-04fb508f534e.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwMjQ2LWYyODVlZWMxLTBkNWMtNDI0Ni1iZDRmLTA0ZmI1MDhmNTM0ZS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zYzEyMTZhN2FmYTg2N2JiNTYzNmZjNjM3ZTE5MmNkMmY3MDVkYzljNDdmZDg0NzVhNThiNDlmYTRmMDhmZDFjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.RZrwh72fV4G7y8IMlyjwVVfg6Rgxgox7sxODk0xeI3s">



</p>
<br />
<h3>&#9316; Enable IIS </h3>
<p> Once the VM is open, the next step is to install / enable IIS. For that, the Control Panel needs to be accessed and the programs applet opened. Under programs, "Turn Windows features on or off" needs to be selected.</p>
<p> <img width="552" alt="6" src="https://private-user-images.githubusercontent.com/163789590/313890306-adbf4223-9ff9-4101-a589-4ef0d8e7796b.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwMzA2LWFkYmY0MjIzLTlmZjktNDEwMS1hNTg5LTRlZjBkOGU3Nzk2Yi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iMDlkMDM3NzVkYzA0ZGM5ZGE0MDVlMTNhZGMyNjE5ZWQyOGE4YmU0ZmIyODZmZGNhMWU3NzZjZTk1MWRiYmYzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.kNNNFTEz7qryqcW_Brc6VoFUL6raI1fhHhoweH3AgQE">


  
</p>
<p>Then, enable and expand the following features:</p>
<p><img width="295" alt="7" src="https://private-user-images.githubusercontent.com/163789590/313890741-26ceaf15-fffc-4fc9-a36c-cf93a237a6b0.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwNzQxLTI2Y2VhZjE1LWZmZmMtNGZjOS1hMzZjLWNmOTNhMjM3YTZiMC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02YjhjMzA1MTcyNmRlNDNjYmZjNjhiZTM3NTc2N2VmYjcwYzU0ZmJkM2U1YWY4ZTFjYWNiMTk0MzA2NzIwNjM1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.ZDCQZKrQDQpLzUm3hYC3Q3qfFE9a6A008sB8MLL1yDE">

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
<img width="1094" alt="8" src="https://private-user-images.githubusercontent.com/163789590/313890806-31cc67ff-0588-4591-b084-16bf4dd457d1.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwODA2LTMxY2M2N2ZmLTA1ODgtNDU5MS1iMDg0LTE2YmY0ZGQ0NTdkMS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNWMzZGUyNGFkNWEwMTRmZTg1ZWZjMDlhNmY2MjI0ODNiZjFkMWNmODRjOTE2ZWZlZmI0NzI2NTVlODBjYTU0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.2VLyQD6bOlBOnVoE2cpPPGBtQvCZkm0KXFcI6vfPJtc">

<br> <br>
<h3>&#9317; Download and Install PHP Manager</h3>
<p> To download and install PHP manager, you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a>(PHPManagerForIIS_V1.5.0.msi) 
</p> <br>
<p><img width="386" alt="9" src="https://private-user-images.githubusercontent.com/163789590/313890900-62dddfb0-16f0-41ed-86f9-3995eb06dd7d.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjAyNDAsIm5iZiI6MTcyMDU1OTk0MCwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkwOTAwLTYyZGRkZmIwLTE2ZjAtNDFlZC04NmY5LTM5OTVlYjA2ZGQ3ZC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTE5MDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1kZGI2MThmMTc1NjU4Y2E3ZTI1OGVhNjQ0Njc1MGEwYzM3MWI4OTJhNjhiNzVmMDhlMThiOTgxZDNjOGY4M2EwJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.nPw1n_Za8sqXZe302cSBLmeVWda473yd_kCTxTUKfBU">

</p> 
<br>
<h3>&#9318; Download and Install the Rewrite Module</h3>
<p>To download and install the rewrite module (rewrite_amd64_en-US.msi), you can by accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> </p>
<p><img width="647 "alt="9" src="https://private-user-images.githubusercontent.com/163789590/313892238-d4eb4f5f-a923-4683-9bf8-cb96869b70b6.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyMjM4LWQ0ZWI0ZjVmLWE5MjMtNDY4My05YmY4LWNiOTY4NjliNzBiNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hZjMxODFjNmFmNzNhMTVhMGI1ODU4NDIwNDJjNzA1MDJhM2M1ZDU2NWMxMjY0ZWQ1ZjY2NmY0NDk2MzZhMWE0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.JuUvI4TZ8DR6m0S6WVPViU6YswOyZpzbIDrQK0Ybmu4">

</p>
<h3>&#9319; Create a new directory</h3>
<p>Continue to File Explorer and create the directory C:\PHP </p>
<img width="647" alt="11" src="https://private-user-images.githubusercontent.com/163789590/313892282-ada44197-55a4-4c96-beba-703156fca967.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyMjgyLWFkYTQ0MTk3LTU1YTQtNGM5Ni1iZWJhLTcwMzE1NmZjYTk2Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hN2FjNmRhYzEyYjk0NmI0MDBlMTZlODUxMDIzOTY1OTc4OTUyNjFkNDVkYmQ2NDQ3NWI5MDYxNzhhNjExZjJjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Aw0Ey_U7LJ7HdWEb5g4cuiyCuBy92drhPlJwTDp4X_E">

<br>
<br>
<h3>&#9320; Download and install php-7.3.8-nts-Win32-VC15-x86.zip </h3>
<p> Download and install php-7.3.8-nts-Win32-VC15-x86.zip, you can be accessing the <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> installation files </a> and unzipping the contents into the newly created folder located at C:\PHP </p>
<img width="631" alt="12" src="https://private-user-images.githubusercontent.com/163789590/313892163-6ad92189-30c6-48ee-a0c0-c4a884130c7f.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyMTYzLTZhZDkyMTg5LTMwYzYtNDhlZS1hMGMwLWM0YTg4NDEzMGM3Zi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04MjM1OWRiNzBmYTY4NDY3YWM3ZTZjNGRjNmQzY2U4NzQ4MTVmYzM5MGM1NDcyYzdhNTlkZDVkOGQ1MWI4ZjU5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.-vGGHSwcgd1hh6kAdAaZ8PwXhLS68ChZbauH4wHkhmE">

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
<img width="383" alt="13" src="https://private-user-images.githubusercontent.com/163789590/313892238-d4eb4f5f-a923-4683-9bf8-cb96869b70b6.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyMjM4LWQ0ZWI0ZjVmLWE5MjMtNDY4My05YmY4LWNiOTY4NjliNzBiNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hZjMxODFjNmFmNzNhMTVhMGI1ODU4NDIwNDJjNzA1MDJhM2M1ZDU2NWMxMjY0ZWQ1ZjY2NmY0NDk2MzZhMWE0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.JuUvI4TZ8DR6m0S6WVPViU6YswOyZpzbIDrQK0Ybmu4">

<br>
<h3>&#9323; Launch IIS as an administrator</h3>
<p> Search for IIS in the Windows search bar and right click it and choose open as Administrator</p>
<br>
<h3>&#9324; Register PHP Manager </h3>
<br>
<img width="682" alt="14" src="https://private-user-images.githubusercontent.com/163789590/313892282-ada44197-55a4-4c96-beba-703156fca967.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyMjgyLWFkYTQ0MTk3LTU1YTQtNGM5Ni1iZWJhLTcwMzE1NmZjYTk2Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hN2FjNmRhYzEyYjk0NmI0MDBlMTZlODUxMDIzOTY1OTc4OTUyNjFkNDVkYmQ2NDQ3NWI5MDYxNzhhNjExZjJjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Aw0Ey_U7LJ7HdWEb5g4cuiyCuBy92drhPlJwTDp4X_E">


<br>
<br>
<p><strong> NOTE: Registration will require you to provide a path to "php-cgie.exe". Direct it to the PHP folder created before and you will locate the file that is being asked for. 
</strong></p>
<br>
<img width="623" alt="15" src="https://private-user-images.githubusercontent.com/163789590/313892349-7dd8ba1b-6709-4b18-8350-b1db5d987228.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyMzQ5LTdkZDhiYTFiLTY3MDktNGIxOC04MzUwLWIxZGI1ZDk4NzIyOC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hMTM1N2E4MjUxZGJmNjYzOTc2MTY0MmM2NmVmZjRkNjEwNzdjZDU4YzcxMDA2M2Q2ODFkYjY0NWEyMDQ0NTEzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.GpYjitX7QbCSZyVRYvPya-R90tesCzo5w4fdgHDNE4U">

<br>
<p>
</p> 
<h3>&#9325; Restart the IIS server</h3>
<p> The restart button can be found on the right side of the window.</p>
<br>
<img width="623" alt="16" src="https://private-user-images.githubusercontent.com/163789590/313892407-11bc6c19-711d-4414-9088-f20551772504.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyNDA3LTExYmM2YzE5LTcxMWQtNDQxNC05MDg4LWYyMDU1MTc3MjUwNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MDFhNTY4YTczNjdkZjhiOTE2MWRlYWMyYTg3ZDBlMmI2NWY1ODY0ODIyMTlhMjE1MTgzNTRjYjQwMDEwYmQzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.564xgk5lck8pPoSIVCTyy7J_Z-kKkOJG0tTTEjtjegU">

<br>
<br>
<h3>&#9326; Download and install osTicket</h3>
<p> Download and install osTicket v1.15.8 from the installation files and extract the contents to c:\inetpub\wwwroot </p>
<br>
<img width="547" alt="17" src="https://private-user-images.githubusercontent.com/163789590/313892707-ce997e99-d53d-4e47-b652-4dccffe7ba93.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyNzA3LWNlOTk3ZTk5LWQ1M2QtNGU0Ny1iNjUyLTRkY2NmZmU3YmE5My5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zMjE5ZGI3ODdmMWIxZDg5Mzg2MjM3YzkwMzk0Y2ZmN2IyN2UwYTU4ZGJjOGU3YzUyMWI0NDc4OTk2MjI3ZGZhJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.dera3pawOaCOA93lRNRlh8U67tUNJQAjLgPS7SJQI58">

<p> Inside c:\inetpub\wwwroot, Rename “upload” to “osTicket”</p>
<br>
<br>
<h3>&#9327; Restart the IIS server again.</h3>
<img width="623" alt="18" src="https://private-user-images.githubusercontent.com/163789590/313892759-5910d134-5bcd-4c12-8b39-02371e6440b4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkyNzU5LTU5MTBkMTM0LTViY2QtNGMxMi04YjM5LTAyMzcxZTY0NDBiNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05OGVjZTM2ZjVhZmIwOTM5MWUyN2RkYjNhZTlmN2NlYjFlZDIwZTRiMjRlMGNmYTg1MGY1NzA4NmZjZTEwMTE5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.mmKpEqFwrkg8aiLFq1ofXGmFIVA_DyGb4n8il2gxFsU">

<br>
<br>
<h3>&#9328; Launch osTicket </h3>
<p>On the left hand side of IIS, Expand on the VM name -> Sites - > Default Website -> osTicket </p>
<img width="623" alt="19" src="https://private-user-images.githubusercontent.com/163789590/313893102-892d71d4-7344-41f9-8c32-3beb4dcb31a9.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzMTAyLTg5MmQ3MWQ0LTczNDQtNDFmOS04YzMyLTNiZWI0ZGNiMzFhOS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iZjJmMDliMjU4OTIyYzBjOWI4OGQ1YmZjNzNmYjM4NDcwMTNlNjEyMmJkN2U4MzJiMDYyNTEwNTRjNjFiOWRjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.yzW9V9CUUE1wxCikM2Bwvl7xGWCztlcrn-aoycgWIA0">

<p></p>
<p><strong>NOTE: Make sure to click on osTicket</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<h3>&#9329; Click on Browse *80 to launch osTicket</h3>
<p> On the right side of the window, click on browse *80 </p>
<img width="623" alt="20" src="https://private-user-images.githubusercontent.com/163789590/313893423-717578c3-c2d8-4c69-bbf1-01ef8de9a606.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzNDIzLTcxNzU3OGMzLWMyZDgtNGM2OS1iYmYxLTAxZWY4ZGU5YTYwNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03OTMwYjFhMGNlNGI0OGJiOGNmMjZkZjhkOGU1YWYzYWFmNTgxODc5Y2NmYmM1YjA1ZjZmZmFjNzI5ZDk5OWMxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.NVOW4mdCsVgYCBBO9maElcSVnSN-igj35CQ3pd1d5eg">

<br>
<br>
<br>
<p><strong>This should the cause the browser to open osTicket</strong>.</p>
<br>
<br>
<img width="664" alt="21" src="https://private-user-images.githubusercontent.com/163789590/313893754-0223308b-1b1e-49b4-b480-64e5c5508e9e.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzNzU0LTAyMjMzMDhiLTFiMWUtNDliNC1iNDgwLTY0ZTVjNTUwOGU5ZS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0yN2UwM2E2MTlhY2Q0MGRiNzIxNGViZGFmM2ExY2IzNzU4ZDI3YWQzNzY3YzY4MTExMDFmYzI2ZDcxNTI1YWM0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.rswRmVM78FrgXUXAb9xUX5URIOKJj8HUqcAC5hU3u4Q">

<br>
<br>
<br>
<h3>&#9330; Enable extensions</h3>
<p>Open IIS and click on PHP Manager and select "enable or disable extension". </p>
<p>Enable the following extensions:</p>
<p>[X]Enable: php_imap.dll</p>
<p>[X]Enable: php_intl.dll</p>
<p>[X]Enable: php_opcache.dll</p>
<img width="273" alt="22" src="https://private-user-images.githubusercontent.com/163789590/313893820-46300aec-3d0c-480c-85ed-d76850928824.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzODIwLTQ2MzAwYWVjLTNkMGMtNDgwYy04NWVkLWQ3Njg1MDkyODgyNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04OGQ0MzMyOTM0YWE0MjVmMzEwN2ZjNTdlNThkNjNhN2UyYTI2ZGY3OGE3NjIyNDIyNWVlNjY2MzYyMGUyYTQ1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.r927-ohegIYKBYJYb7UBZYLh1pCjovQiANoq1OKJiqU">

<br>
<br>
<br>
<h3>&#9331; Refresh osTicket</h3>

<p>Refresh the osTicket page on the browser and notice some extensions will now appear active.</p>
<img width="608" alt="23" src="https://private-user-images.githubusercontent.com/163789590/313893884-8987ca1e-de41-46ef-9a5f-45cef20fead4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzODg0LTg5ODdjYTFlLWRlNDEtNDZlZi05YTVmLTQ1Y2VmMjBmZWFkNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zNzhlNDVhY2Q0ZjQ4MTU1NGU0ZTZkMjMzMDQ1MTVjMTYwMWU1N2QyNmMxZTYwN2Y0YzY1Zjg0OWNhM2EwMTk2JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.iiFZLo75m-ErIpGXLKGrFWKPtLzg6PFDjzaU4VxDWEk">

<br>
<br>
<br>

<h3>&#12881; Rename ost-config.ph</h3>

<p> Under C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, rename "ost-sampleconfig.ph" to "ost-config.ph"</p>
<img width="527" alt="24" src="https://private-user-images.githubusercontent.com/163789590/313893930-dbbd4551-331c-4ed5-bce1-abf405a9381b.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzOTMwLWRiYmQ0NTUxLTMzMWMtNGVkNS1iY2UxLWFiZjQwNWE5MzgxYi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01Mjg4MDY2OGE3NGFjMTllM2IxYTQ0ZGNiM2NiNzYyOGNjMTJhZTkyYzM4MmI0ZmZhOTNmZDZkMWMwZTY3NWUwJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.HY_WU4n9jP3MlsvixZ1Ufd-S2R9gwqDk_k3HG4VpMBE">

<br>
<br>
<br>

<h3>&#12882; Configure ost-config.ph permissions</h3>

<p>Configure ost-config.php permissions by right-clicking and choosing</p>
<p>Properties -> Security -> Advance -> Disable inheritance</p> 
<p>Choose remove all inherited permissions and add everyone as a principal. Choose all boxes to make sure all permissions are given. </p>
<img width="571" alt="25" src="https://private-user-images.githubusercontent.com/163789590/313893991-9d82210c-f2c6-4666-81bd-eca5c636a6b2.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODkzOTkxLTlkODIyMTBjLWYyYzYtNDY2Ni04MWJkLWVjYTVjNjM2YTZiMi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05MGQzMGJhZTgyYjkyZTVjM2Y5ZDQ1MWNlNzMzMGMyMTAxNzVhNWQ0NzMxOGU0ZTRhMzc4MTE4YjM1YzAzNDI0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.fVDGTdBpe50kqaRzG_ULLw5TcgjcvFZcY4yaJj4Y9VE">

<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12883; Proceed with the osTicket installation</h3>

<p> Proceed with the osTicket installer on your browser by completing the first half of the page.</p>
<img width="611" alt="26" src="https://private-user-images.githubusercontent.com/163789590/313894079-a6745182-4138-4529-88ec-ffdf279dd78c.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODk0MDc5LWE2NzQ1MTgyLTQxMzgtNDUyOS04OGVjLWZmZGYyNzlkZDc4Yy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jMWY1ZjAzYjIwMDk2MDljMjI2NGJlNWE3MjY4OWQxNWZkYjcyNDI1ZjVhY2IyZmY1OGNjZDk3ZDI5OGM1YmU2JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.7SQLV8DMln2n14qMAl3XmHS_Wiy0Dt8EQ82X7ZKNRpc">

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
<img width="512" alt="27" src="https://private-user-images.githubusercontent.com/163789590/313894173-33b7f850-73a3-489a-8ccf-60f50d6fe94b.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODk0MTczLTMzYjdmODUwLTczYTMtNDg5YS04Y2NmLTYwZjUwZDZmZTk0Yi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05Y2MyZmQ2MTE4YzA5ZGYzYzI0NjY5ZGQ1OTg0MDUxYjhkNDgxMjkyOTViZDNhN2Y5YjA2ZjkzM2JjNGI5ZmEzJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.lvfPh8MI181HsI4UgIfoQ8xfS2V_kI_a_iNj__2EnJY">

<br>
<br>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#12886; Complete the signing up process</h3>

<p>Return to the osTicket browser and complete the missing credentials. 
It should look something like this.</p>
<img width="308" alt="28" src="https://private-user-images.githubusercontent.com/163789590/313894199-13d08112-2396-4c73-9a1e-c8300a1d160c.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjA1NjA2MzYsIm5iZiI6MTcyMDU2MDMzNiwicGF0aCI6Ii8xNjM3ODk1OTAvMzEzODk0MTk5LTEzZDA4MTEyLTIzOTYtNGM3My05YTFlLWM4MzAwYTFkMTYwYy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzA5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwOVQyMTI1MzZaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iMmRmZmQwZGM5NGIzMjI3NmI5MGUyNjI0MjRhNzFlMmEzZjVlYTBmOTQ0ODNiZmRiNGNiNzQyNDAyNTM0MTI3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.gdMI6qP7qZsGQODINaGMvQCtWo7Qk-IHif_GYBWrvtc">


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
