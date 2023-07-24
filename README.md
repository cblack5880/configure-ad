<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Building Azure accounts- resource group and virtual machines.
- Install Active Directory
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>


![image](https://github.com/cblack5880/configure-ad/assets/138612466/f0059d2d-562c-4c13-86d3-904acb93c816)

![image](https://github.com/cblack5880/configure-ad/assets/138612466/84bb0584-2a80-46c2-9517-7dd442220fbc)

![image](https://github.com/cblack5880/configure-ad/assets/138612466/f8057fef-a6db-46ef-a1d0-bdf282e7e0c4)
Changing Domain Controller IP address to Static


<h2>Install Active Directory</h2>

The following pictures will show this:

Login to DC-1 and install Active Directory Domain Services

Promote as a DC: Setup a new forest as mydomain.com

Restart and then log back into DC-1 as user: mydomain.com\labuser

![image](https://github.com/cblack5880/configure-ad/assets/138612466/e7b0fbab-fdb1-445e-87e4-f4c329cfd35f)
Install Active Directory from Server Manager in DC-1.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/b82c4cb3-21dd-44e8-b7bc-8d9941ebe22a)
Click here to promote the server to a Domain Controller.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/b0f64109-2def-465d-bb41-0ad3126e09c5)
Setting up a new forest/ domain name that all users would use to login.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/3ea721ff-8467-4333-bc7b-84c03abe7294)
DC-1 Remote desktop will close after installing new forest. When you open it again, you would have to use "mydomain.com\labuer" to login.



# configure-ad
