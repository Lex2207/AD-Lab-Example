#Active-Directory-Lab
<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop (Domain Controller Database VM & Windows 10 VM)
- Active Directory
- DNS

<h2>Active Directory Prerequisites</h2>

- 2 VMs connected on the same Network (DC-1 = Domain Controller Database VM) (Client-11 = Windows 10 VM)
<p>
<img src="https://i.imgur.com/pBOmABq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Make sure the Domain Controller (DC-1) VM has a static DNS IP address so that it will not change when our client tries to query our database for information.
<img src="https://i.imgur.com/KMe6Sfp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- I enabled the ICMP traffic within the Domain Controller's firewall in order for me to check the connectivity between the two systems 
<p>
<img src="https://i.imgur.com/2KKluYk.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/sAn3el0.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

- Install Active Directory
<p>
<img src="https://i.imgur.com/iTmjUFE.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/0OsZkUf.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/7lNoH2B.jpg" width="80%" alt="Disk Sanitization Steps"/>
</p>


Check to make sure the client VM has been joined to the Domain Controller (using the DC DNS static IP) so the Client can use the DC DNS as its primary server.
This is the ipconfig /all command on the Client VM before assigning the right DNS IP
<p>
<img src="https://i.imgur.com/grR9PaH.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
I went into my Microsoft Azure portal to change the client VM DNS IP to the static IP we configured earlier within our DC-1 VM azure poratl.
<p>
<img src="https://i.imgur.com/f7ZMrVo.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Once that is done, we can see the the DNS has been changed to the correct IP in our client command prompt.
<p>
<img src="https://i.imgur.com/ijLUQl2.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
Lastly, add client-11 to the Domain Controller
<p>
<img src="https://i.imgur.com/Ab85vGJ.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<p>
This section will show an example of creating a group with permissions for a user to access a file. I will try to access the "accounting folder" with my user without persmissions first. As you can see, the error shows I do not have permission to view this file yet as my user ( random user created for lab = bek.jet) </p>
<br 
<p>
<img src="https://i.imgur.com/cdporem.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

I added the "ACCOUNTANTS" group with the proper permissions for the accounting file (Read & Write)
<p>
<img src="https://i.imgur.com/HAv126Z.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Rt7UQq7.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Add the user I want to be able to access the file. 
<p>
<img src="https://i.imgur.com/UQ07Zkw.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Lasty, I log back in with the user I have put into the correct group with permissions to view and modify the accounting file.
<p>
<img src="https://i.imgur.com/L6vbY9S.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Finally I was able to open the accounting file and view the contents.
<p>
<img src="https://i.imgur.com/af6HpWK.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


