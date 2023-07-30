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
Setting up a new forest/ domain name that all users would use to log in.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/3ea721ff-8467-4333-bc7b-84c03abe7294)
DC-1 Remote desktop will close after installing new forest. When you open it again, you would have to use "mydomain.com\labuer" to login.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/78261750-4547-47f7-bba0-32786acf33f8)

Once, DC-1 is back opened, Click tools and open Active Directory Users and Computers
You would also create 2 organizational units - Employees and Admins.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/2498fe3f-7d7e-499a-8a6f-bf1b0109ae75)

Right-click in _Admins box to create a New user. There will be more settings to select after creating the user.
You would have to right-click the user and go to properties, and add the user to a domain. This shows that I'm adding the user to "Domain Admins". 

![image](https://github.com/cblack5880/configure-ad/assets/138612466/2e6f8ef0-a960-407e-b1da-d13b398ded5d)

Now I'm going to Log out/close the Remote Desktop connection to DC-1 and log back in as “mydomain.com\jane_admin”.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/7318cbda-4dab-4fd5-b3cc-cf807eebe53b)

Next I will set Client-1’s DNS settings to the DC’s Private IP address.

![image](https://github.com/cblack5880/configure-ad/assets/138612466/cca88262-b560-4e50-a5fe-bb40ae6e8950)
![image](https://github.com/cblack5880/configure-ad/assets/138612466/a1a64c89-4969-4817-b911-ff5d79a497d8)
![image](https://github.com/cblack5880/configure-ad/assets/138612466/61e91a11-a870-4951-8e7c-770cd2bf68e4)

Now I will restart  Client-1 virtual machine from Azure
When Clent-1 is back up, Remane your pc to Mydomain in the domain section. From there, you would put in the my domain credentials for Jane_admin. 

![image](https://github.com/cblack5880/configure-ad/assets/138612466/3a25afe7-add6-4925-8746-db85d8db74a4)


# configure-ad
