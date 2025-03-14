# AD-Within-Azure
<p align="center">
  
![Azure](https://github.com/user-attachments/assets/86350ec7-d80e-4912-b9af-52d7a51cf3a9)

</p>

<h1>Active Directory - A Guide</h1>
This Guide Outlines how to Configure ActiveDirectory <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (22H2)
- Microsoft Windows Server

<h2>List of Prerequisites</h2>

- Domain Control (DC)
- Client (Windows VM)
  
<h2>Steps</h2>

<p>
  

![AD1](https://github.com/user-attachments/assets/db084b17-6241-4e67-a13c-88915441bac0)

</p>
<p>
Consistency in network service is key
for other servers, clients, and network devices who rely on the DC’s IP for authentication and DNS resolution. A changing IP could cause disruptions.
It is also for remote access stability
for when remotely connecting to the DC, a static IP ensures a reliable connection without needing to track address changes.
It also helps in prevention of authentication failures.
Active Directory and other domain services depend on a fixed IP to function properly. DHCP changes could cause logon and replication issues. So in order to ensure a smooth connection, the domain controller's IP is going from a dynamic one to a static address.

</p>
<br />
<p>

![AD2](https://github.com/user-attachments/assets/d8a58363-43af-430b-b14f-4c918d5ca95e)


</p>
<p>
When you set a server’s DNS address to the private IP address of the Domain Controller instead of a virtually provided address, you ensure that all DNS queries are processed within the local network rather than relying on an external or dynamically assigned address.This ensures the functionality of Active Directory, and faster response times. </p>
<br />
<p>


![AD 3-5](https://github.com/user-attachments/assets/7036e6f5-f94d-4c37-8a09-3bde20684bf3)


</p>
<p>
For Final Verification:
Run ipconfig /all to confirm that the DC's private IP is set as the DNS.
</p>
<br />

