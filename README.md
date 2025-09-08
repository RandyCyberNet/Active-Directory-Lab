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
- <b>Shadow Volume Copy</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Windows Server 2025</b> (24H2)
- <b>Oracle VirtualBox</b>

<h2>Program walk-through:</h2>

<p align="center">
The Network Topology diagram: <br/>
<img src="https://imgur.com/uDROi1p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
install windows server 2025 into Vbox:  <br/>
<img src="https://imgur.com/4hBtQeW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Importatn network configurations (network adaptors): <br/>
<img src="https://imgur.com/x6avdkf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once windows server is up, change the deafult name of the system and go to network adaptors and determine which one is connected to the public and internal networks and label them. APIPA will be the internal network:  <br/>
<img src="https://imgur.com/F47Rskt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
configure the internal netowork to have a static IP address and a loop back DNS server:  <br/>
<img src="https://imgur.com/FdJ73zZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/06As9zU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://imgur.com/lyimecE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/qWsTj1u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/hwmWoAT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/0VCFypl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/qQ6HtOB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/GL709TC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/GOh20x4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/A3ycBZZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/516A2N6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/wBOg6MB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/CN3jgW6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/KveyzvO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/hKETq77.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/iMpNnZa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Install necesary software to have Active direcotry on the DC :  <br/>
<img src="https://imgur.com/UyfhZhO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
