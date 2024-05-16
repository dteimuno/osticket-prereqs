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

- Create Resource Group in Azure
- Create Windows  10 Virtual Machines with 2-4 virtuals CPUs

<h2>Installation Steps</h2>

<p>
<img width="1200"  alt="Screenshot 2024-05-15 at 11 42 46 PM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/dea09936-a271-4024-8711-26876d0d8ef8">
</p>
<p>
You must first create a resource Group in Azure to hold all the relevant resources that will  be used for this lab.To do so, Go to the Azure Portal, search for 'Resource  Groups', and  then  click on 'Resource Groups'. Enter a name for the resource group, select wherre you would like for resource group to be hosted( Region), and click review + create. Should you successfully do this you should see results like this below:
  
<img width="80%" height="80" alt="Screenshot 2024-05-15 at 11 44 38 PM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/f96bb618-cc2f-4f84-bebf-46f6b0a418d2">
</p>
<br />

<p>
<img width="80%" height="80" alt="Screenshot 2024-05-15 at 11 53 05 PM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/1ce1b22d-0685-4c75-898e-067d5558917e">
</p>
<p>
To create Virtual Machine, in Azure search for virtual machines and click on it. Input a name for the virtual machine and select a region, image, and image size. Additionally, select a username and password:

<img width="80%" height="80" alt="Screenshot 2024-05-15 at 11 53 20 PM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/c6ff7704-907b-45ac-906e-ce3823189be8">


Click Review+Create and click create after the validation passes to start the VM creation process.
</p>
<br />
<p>
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 01 07 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/aa0f102b-c55f-44b8-a869-6f9ab48dc621">
</p>
<p>
Once the deployment is complete go to the VM and obtain the IP address for the VM to be able to log in via Remote Desktop. Go to Microsoft Remote Assistance, add the IP address and connect:

<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 06 19 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/ce35beab-815d-49ac-b5b0-8bec2947cdf0">

Enter your login credentials to sign in to the VM
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 06 56 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/872534cb-df38-4109-ad96-373a7ad574eb">

</p>
<br />

<p>
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 23 03 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/59927541-aea9-4014-ba15-5cbdca0aa346">
</p>
<p>
Install and enable Internet Information Services with CGI. In your VM go to control panel>Programs>Turn Windows Features on or off>Check Internet Information Services>check Application Development Features> Check CGI.

Decompress Common HTTP Features>check all files underneath. Click OK
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 23 20 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/e1b47fa4-5b39-4769-9a5b-42426b886bed">

To confirm installation of IIS, in a web browser type 127.0.0.1. If successful, your page should look like this:
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 28 03 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/b6eb18fd-c0c3-4c44-8f33-c1196a9d9bed">

</p>
<br />

<p>
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 12 37 03 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/cf6f0f99-71de-47ba-b80e-6f430d4d2ccd">
</p>
<p>
Download and install PHP Manager for IIS.

Download and install the Rewrite Module. 

Create directory C:\PHP
Download PHP 7.3.8 and extract the files into C:\PHP. When complete the C:\PHP folder should look like this:
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/3e704fdf-c58e-4fca-a04e-5286f82611ec">

Download and install VC_redist.x86.exe
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 06 52 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/a5582c75-f4fa-4e03-b741-a6b673596282">

Install mySQL 5.5.62. Select a Typical installation and click install to complete installation.
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 09 43 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/7614342d-6b84-497c-b6bd-3e5f4128a735">

<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 11 46 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/9ec3563b-f772-4a11-9255-1931e0925c91">

<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 12 11 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/eeae32ca-1833-48fe-a804-1d63f3653ca3">

<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 12 47 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/ef95a461-6d50-44f5-a0e6-3c6e00c05cb0">

Finish installation:
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 16 29 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/8f6bcee3-7289-45cf-b618-d374a14fa217">

Open IIS as an administrator
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 20 00 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/ca96a9af-eed3-4f8c-adfb-df7feb13f362">

Register PHP from within IIS
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 24 12 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/31d52d12-7217-47b3-8af1-9003bd0e8457">

<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 26 15 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/434b0a93-1186-4537-b012-ff0957abf2f3">

Restart IIS server
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 27 57 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/8550a807-6eef-4ff5-bc6e-d0eb85453848">

Download OS ticket from Installation files folder. Open folder and move the file 'upload' to C:\inetpub\wwwroot
<img width="80%" height="80" alt="Screenshot 2024-05-16 at 1 33 46 AM" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/95f5f13e-ce93-4e59-97cb-156d6035c4b4">

Rename upload folder to osTicket and restart osTicket

Go to site>Default>osTicket>browse *80. Click it. End result should be:
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/79c1feb0-71ec-4aff-ba25-7fd08d1c346c">

Note that some extensions are not enabled
-Go back to IIS, sites -> Default -> osTicket
-Double-click PHP Manager
-Click “Enable or disable an extension”
-Enable: php_imap.dll
-Enable: php_intl.dll
-Enable: php_opcache.dll
-Refresh the osTicket site in your browse, observe the changes
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/101f306b-51a1-429c-91c8-3dc557057bee">

Rename: ost-config.php
-From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
-To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/59dccf97-b438-4d1c-9158-b57bf7cf9cde">

Assign Permissions: ost-config.php
-Disable inheritance -> Remove All
-New Permissions -> Everyone -> All
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/30987e82-c65d-4e7f-bbd2-19f12a92a954">


Continue Setting up osticket in the browser
-MySQL Database: osTicket
-MySQL Username: root
-MySQL Password: Password1
-Click “Install Now!”
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/9ee796a5-d4f4-4867-87d2-dc0e1e62ec8f">

Clean up
-Delete: C:\inetpub\wwwroot\osTicket\setup
-Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img width="80%" height="80" alt="image" src="https://github.com/dteimuno/osticket-prereqs/assets/169619672/5389a884-2ab3-4b77-a0f8-6ca99ae5f2f9">
