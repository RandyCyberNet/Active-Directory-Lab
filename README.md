<h1>🖥️Active Directory Lab</h1>

<h2>Description</h2>
This project demonstrates the setup and configuration of a Windows Active Directory home lab designed to simulate enterprise-level identity and access management.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell Scripts</b> 
- <b>Windows Domain Controller</b>
- <b>Active Directory Users and Computers</b>
- <b>Organizational Units & Delegation</b>
- <b>Group Policy Objects</b>
- <b>Networking Configurations (TCP/IP, DNS, DHCP settings)</b>
- <b>Using SMB for File Sharing</b>
- <b>File Sharing Permissions & Access</b>
- <b>Shadow Volume Copy</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows Server 2025</b> (24H2)
- <b>Oracle VirtualBox</b>

<h2>Program walk-through:</h2>

<p align="center">
The Topology diagram: <br/>
<img src="https://imgur.com/uDROi1p.png" height="80%" width="80%"/>
<br />
<br />
(Inside VBox Windows 2025 Server) Checking which network card is the internal one (will have an APIPA address), and labeling each one either public or internal.  <br/>
<img src="https://imgur.com/4hBtQeW.png" height="80%" width="80%"/>
<br />
<br />
<br/>
<img src="https://imgur.com/x6avdkf.png" height="80%" width="80%" />
<br />
<br />
Assigning a static IPv4 address to the Internal card, which will also be the default gateway for the CLIENT1. Then I loop back the DNS server to use itself as a resolver, since I will configure an AD forest and the process typically installs the DNS server role on the first Domain Controller. This allows for self-sufficiency and redundant DNS resolution.
<br/>
<img src="https://imgur.com/F47Rskt.png" height="80%" width="80%" />
<br />
<br />
Here I install the software necessary for a DC, and then create a new forest when prompted to promote the DC server.<br/>
<img src="https://imgur.com/FdJ73zZ.png" height="80%" width="80%" />
<br />
<br />
Then I create a new user (myself) to have admin controls instead of using the default admin account from the DC. <br/>
<img src="https://imgur.com/06As9zU.png" height="80%" width="80%" />
<br />
<br />
Next, I installed RAS and NAT to allow CLIENT1 to have Internet access in this “private VM Network." <br/>
<img src="https://imgur.com/lyimecE.png" height="80%" width="80%" />
<br />
<br />
I then install the DHCP software to configure the DC server to hand out IPv4 addresses, giving it a range of 172.16.0.100–200. <br/>
<img src="https://imgur.com/qWsTj1u.png" height="80%" width="80%" />
<br />
<br />
Next, I create an SMB file-sharing folder using a disk volume (Shared Drive) for other users to access a shared network folder. I also configured Volume Shadow Copy (Backup, shared main) for redundancy and set it to back up at the end of the day at midnight.  <br/>
<img src="https://imgur.com/hwmWoAT.png" height="80%" width="80%" />
<br />
<br />
I then created OUs and added security groups for:
AllAdmins = Stores all admins from all IT operations (Filesharing/lab/server/etc)
AllUsers = Stores all users (employees/Interns/Managers/etc)
Security Groups
Admin Groups = Contains different IT Admin security groups, which allows adding or removing members from these groups.
UserGroups = Contains different security groups, like Finance Interns group, Marketing Interns group, Finance employees group, etc.
SharedFolder (Employees)
Finance Managers/employees = Group with the finance employee group
IT admins/employees = Group with the IT employees/admins group
Marketing managers/employees = Group with the marketing managers/employees group
Shared Folder (Interns)
Finance = Group with only the Finance Interns group
IT = Group with only the IT Interns group
Marketing = Group with only the Marketing Interns group <br/>
<img src="https://imgur.com/0VCFypl.png" height="80%" width="80%" />
<br />
<br />
Created separate folders for the Finance, Marketing, and IT interns. Gave them full control except for Delete, Change Permissions, and Take Ownership permissions. I also added access for the corresponding security group to each folder (Marketing group access only to the Marketing folder, Finance group access only to the Finance folder, etc).  <br/>
<img src="https://imgur.com/qQ6HtOB.png" height="80%" width="80%" />
<br />
<br />
Created a mapped Shared Folder for all users to access the shared network folder and their respective files. <br/>
<img src="https://imgur.com/GL709TC.png" height="80%" width="80%" />
<br />
<br />
Configured the account lockout threshold to 3 attempts before lockout.<br/>
<img src="https://imgur.com/GOh20x4.png" height="80%" width="80%" />
<br />
<br />
Implemented and ran a PowerShell script to create 50 new users, store them in the AllUsers OU, and assign them a default password. <br/>
<img src="https://imgur.com/A3ycBZZ.png" height="80%" width="80%" />
<br />
<br />
<br/>
<img src="https://imgur.com/516A2N6.png" height="80%" width="80%" />
<br />
<br />
Using the CLIENT1 computer, I logged in with a random user the script created. <br/>
<img src="https://imgur.com/wBOg6MB.png" height="80%" width="80%" />
<br />
<br />
I manually put Maria into the MarketingInterns security group, in the DC computer, and set to only be able to access the MarketingInterns folder (tested successfully).  <br/>
<img src="https://imgur.com/CN3jgW6.png" height="80%" width="80%" />
<br />
<br />
<br/>
<img src="https://imgur.com/KveyzvO.png" height="80%" width="80%" />
<br />
<br />
Also ensured that Maria and the other users created did not have administrative permissions. <br/>
<img src="https://imgur.com/hKETq77.png" height="80%" width="80%" />
<br />
<br />
Finally, I checked to ensure CLIENT1 and the users connected to it had Internet access through the DC server. <br/>
<img src="https://imgur.com/UNXTlNL.png" height="80%" width="80%" />
<br />
<br />
<br/>
<img src="https://imgur.com/iMpNnZa.png" height="80%" width="80%" />
<br />
<br />
<br/>
<img src="https://imgur.com/UyfhZhO.png" height="80%" width="80%" />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
