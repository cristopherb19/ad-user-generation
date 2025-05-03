<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Generating Users in Active Directory</h1>
Welcome back again!  In this project we will focus on populating our domain by generating numerous users.  This project is a bit shorter but it is an integral part to our goal of simulating multiple scenarios that can occur when using Active Directory.
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>Prerequisites</h2>

-  Please complete the following before beginning this project:
    - <a href="https://github.com/christianDCdev/active-directory-setup">Setup for Active Directory Infrastructure</a>
    - <a href="https://github.com/christianDCdev/ad-deploy-and-config">Active Directory Deployment and Configuration</a>

<h2>Objectives</h2>

- Populate our domain by creating additional users

<h2>Project Steps</h2>

<h3>&#9312; Login to DC-1 VM</h3>
<p>

- Login to DC-1 VM via Remote Desktop as "Jane Doe" (username: jane_admin)
  
</p>

<h3>&#9313; Use PowerShell to Create Users</h3>

<p>

- Within DC-1 VM, open "Windows PowerShell ISE" application as an administrator
- Create a new file, if one is not already displayed
- Copy and paste the contents of this <a href="https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1">script</a> into PowerShell ISE file, then save it
<img src="https://i.imgur.com/9ly2Mmp.png" height="80%" width="80%" alt="Script"/>

- Run script by clicking the green play button at the top
<img src="https://i.imgur.com/ArZTgBd.png" height="80%" width="80%" alt="Run script button"/>

- Observe the users being created in the PowerShell command-line interface
<img src="https://i.imgur.com/j1xJ89h.png" height="80%" width="80%" alt="Users created in CLI"/>

</p>
<br />

<h3>&#9314; Verify in Active Directory that user have been successfully created</h3>

<p>

- Once script is done running, open "Active Directory Users and Computers" application
- Find the "_EMPLOYEES" folder
- Right click folder and select "Refresh" to see if the users have been created
<img src="https://i.imgur.com/S2oIuQm.png" height="80%" width="80%" alt="Users in Active Directory"/>
  
</p>
<br />

<h3>&#9315; Login as one of the newly created users</h3>

<p>

- Choose any newly created user from the Active Directory list
- To ensure the script has worked, you can try to log in to Client-1 VM as the user you chose
  - Example: If the name of the user you chose is "lewa.juwa", then the login username will be "mydomain.com\lewa.juwa"
  - NOTE: The password can be found at the top of the script.  It will be the same for all users.
  
</p>
<br />

<h2>Conclusion</h2>

<p>
  
Congratulations on completing this project!  After generating numerous users into your domain, you have now created an environment in Azure that is capable of simulating various scenarios.  These scenarios are meant to better your understanding of what can be done within Active Directory.

- If you would like to continue to the next step in this series of Active Directory projects, please click <a href="https://github.com/christianDCdev/ad-practical-scenarios">here</a>

</p>
