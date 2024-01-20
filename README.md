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
The Domain Controller VM after restarting now shows the administrator account with the domain name that was assigned:  <br/>
<img src="" height="80%" width="80%" alt="Domain Controller VM information"/>
<br />
