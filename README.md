# AD-Lab-Example
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (Domain Controller Database VM & Windows 10 VM)
- Active Directory
- DNS

<h2>List of Prerequisites in Order to use Active Directory with the correct configurations.</h2>

- 2 VMs connected on the same Network (DC-1 = Domain Controller Database VM) (Client-11 = Windows 10 VM)
<p>
<img src="https://i.imgur.com/XHsyIVF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Make sure the Domain controller VM has a static DNS IP address in order for our client obatin the correct information from the DNS server
<p>
<img src="https://i.imgur.com/KMe6Sfp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Check the Firewall on the Domain controller is set to enable the ICMP traffic in order for us to check the connectivity between the two systems 
<p>
<img src="https://i.imgur.com/q22RmfK.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/sAn3el0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Install Active Directory
<p>
<img src="https://i.imgur.com/iTmjUFE.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/CU0jsZ7.jpg" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/2jNoe6q.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Check to make sure that the client VM has been joined to the Domain Controller (using the DC DNS static IP) so the Client can use the DC DNS as its primary server.
<p>
<img src="https://i.imgur.com/MiHCb27.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

This is the ipconfig /all command on the Client VM before assigning the right DNS IP
<p>
<img src="https://i.imgur.com/zaEV0Fh.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Here I went into Microsoft Azure to change the client VM DNS IP to the static IP we configured earlier within our DC-1 VM
<p>
<img src="https://i.imgur.com/nfqB44u.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Once that is done, we can see the the DNS has been changed to the correct IP in our client command prompt.
<p>
<img src="https://i.imgur.com/qUhu3B6.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>



<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

