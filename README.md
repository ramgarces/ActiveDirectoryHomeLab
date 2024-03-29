<h1>Active Directory Home Lab</h1>

<h2>Description</h2>
In this project I will set up a Windows 10 Active Directory Home Lab using Oracle VirtualBox. The first part of the project will consist of setting up the Virtual Machines (VMs) for the Domain Controller and the client that will utilize the Domain Controller. The second part of the project will be adding user accounts using PowerShell.

<h2>Programs and Utilities Used</h2>

- <b>PowerShell</b>
- <b>Oracle VirtualBox</b>

<h2>Environments Used</h2>

- <b>Windows 10 (21H2)</b>
- <b>Server 2019</b>

<h2>Going through the Lab</h2>

<p align="center">
Creating the Domain Controller VM: <br/>
<img src="https://i.imgur.com/73NlqYC.jpg" height="80%" width="80%" alt="Domain Controller VM creation"/>
<br />

<p align="center">
Information for the Domain Controller VM before finishing creation:  <br/>
<img src="https://i.imgur.com/b7FGJG6.jpg" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Creating an internal network adapter on the Domain Controller VM:  <br/>
<img src="https://i.imgur.com/Sshr42y.jpg" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
After creating the internal network card, I started the Domain Controller, identified the different cards, and renamed them appropriately:  <br/>
<img src="https://i.imgur.com/YibBu5H.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Renaming the Domain Controller VM to something more simple:  <br/>
<img src="https://i.imgur.com/Ch2ZlQC.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Configuring the IP addressing for the internal NIC:  <br/>
<img src="https://i.imgur.com/m1tRsYG.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Beginning the process of installing the Active Directory Domain Services:  <br/>
<img src="https://i.imgur.com/fWIx1fY.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Adding the features for the Active Directory Domain Services:  <br/>
<img src="https://i.imgur.com/xmENhDu.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Active Directory Domain Services have been installed on the Domain Controller:  <br/>
<img src="https://i.imgur.com/yJxz0Sv.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
After the feature installation some Post-deployment Configuration must be done. This can be found on the top right of the Server Manager window indicated by a flag and a yellow notification icon:  <br/>
<img src="https://i.imgur.com/yjZmHQu.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Going through the Post-deployment configuration which includes adding and naming a new forest on the domain:  <br/>
<img src="https://i.imgur.com/EU2SEGu.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Finishing the Post-deployment configuration process:  <br/>
<img src="https://i.imgur.com/i7pElcz.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
The Domain Controller VM after restarting now shows the administrator account with the domain name that was assigned:  <br/>
<img src="https://i.imgur.com/GR5W2vq.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Now, to create an administrator account separate from the default administrator account a new Organizational Unit (OU) is created:  <br/>
<img src="https://i.imgur.com/lJVbxfQ.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
A new user is then created inside the new OU:  <br/>
<img src="https://i.imgur.com/MblmvrY.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Creating the new user account (the 'a' is to indicate it is an administrator account):  <br/>
<img src="https://i.imgur.com/XObvrw6.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
The new account is then added to the 'Domain Admins' group from the properties in order to give it administrative rights:  <br/>
<img src="https://i.imgur.com/5KktJop.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Logging into the new administrator account on the DC:  <br/>
<img src="https://i.imgur.com/f0dvDCU.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Next, RAS and NAT are being installed so that the client VM can access the normal internet through the DC:  <br/>
<img src="https://i.imgur.com/Y12X9ZM.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Navigating to 'Routing and Remote Access' after the installation finished:  <br/>
<img src="https://i.imgur.com/OQp1iT3.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Beginning the process of enabling and configuring Routing and Remote Access:  <br/>
<img src="https://i.imgur.com/eqfDSui.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Configuring the NAT option through the Routing and Remote Access Server Setup Wizard:  <br/>
<img src="https://i.imgur.com/sjwixVl.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Selecting the NIC that will be used for access to the Internet:  <br/>
<img src="https://i.imgur.com/tYBVe6R.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
The Routing and Remote Access (NAT) setup is complete and is indicated by a green arrow on the DC icon in the window:  <br/>
<img src="https://i.imgur.com/xyA6g4l.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Beginning the process of installing a DHCP server role on the DC:  <br/>
<img src="https://i.imgur.com/YEDEWL8.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Configuring the new scope that the DHCP server will assign addresses from:  <br/>
<img src="https://i.imgur.com/kGCQlX2.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
During the DHCP configuration options, the DC's IP address is added as the router used by clients:  <br/>
<img src="https://i.imgur.com/Zh1n9yR.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
The scope now appears in the DHCP role window:  <br/>
<img src="https://i.imgur.com/WsAlDAe.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Next, PowerShell will be used to generate accounts with random names. This is a screenshot of a portion of the names in the file that will be used:  <br/>
<img src="https://i.imgur.com/zhiOtkL.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Here is the PowerShell script used to generate the accounts from the names file:  <br/>
<img src="https://i.imgur.com/ug7ClL8.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
After the PowerShell script has finished running, the _USERS OU can now be seen in Active Directory, and inside that OU all of the new user accounts have been created:  <br/>
<img src="https://i.imgur.com/F1mOiDn.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Now, a client VM is created that will utilize the DC:  <br/>
<img src="https://i.imgur.com/liQIPhL.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Windows 10 <strong>Pro</strong> is installed on the client VM since it is the version of Windows that can join the domain:  <br/>
<img src="https://i.imgur.com/PsRSobZ.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Creating a local user account on the client VM:  <br/>
<img src="https://i.imgur.com/gUNgZnv.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
The DC (in the backround) and the Client VMs running simultaneously, showing the Client VM network configuration:  <br/>
<img src="https://i.imgur.com/2M8aQ6G.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Running some pings on the Client VM to test connectivity to the internet:  <br/>
<img src="https://i.imgur.com/omTBQFt.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Renaming the Client PC and joining the domain from the System Properties:  <br/>
<img src="https://i.imgur.com/8Am2Vog.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
The Client VM has successfully joined mydomain.com:  <br/>
<img src="https://i.imgur.com/R2jwjwD.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
An IP address has been leased to the client and can be seen from the DHCP window on the DC:  <br/>
<img src="https://i.imgur.com/nR3GFiT.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Now, one of the user accounts created earlier in the lab can be used on the Client VM to login to the domain:  <br/>
<img src="https://i.imgur.com/dqTmKVG.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />

<p align="center">
Using <code>whoami</code> in command line to confirm that the account is signed in through the domain on the Client VM:  <br/>
<img src="https://i.imgur.com/W10lasD.png" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />
