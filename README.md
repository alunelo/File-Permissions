<p align="center">
<img src="https://imgur.com/fo2lGUz.png" alt="Traffic Examination"/>
</p>

<h1>Network File Shares and Permissions</h1>
This project explores <b>Domain Name System (DNS)</b> management and analysis using <b>PowerShell, CNAME records, and Windows Server Manager</b>. The goal was to observe how DNS resolves domain names, analyze different record types, and use PowerShell commands to interact with DNS settings efficiently. <br />


<h2>Environments and Technologies Used</h2>

- <b>Microsoft Azure</b> (Virtual Machines/Computer)
    - <b>"CLIENT 1"</b> (User PC) & <b>"DC-1"</b> (Domain Controller PC)
- <b>Remote Desktop</b>
- <b>NTFS (New Technology File System)</b>

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>Key Observations</h2>

- <b>DNS Resolution Analysis</b> – Used PowerShell to query and analyze how domain names resolve to IP addresses.
- <b>CNAME Record Configuration</b> – Created and tested a CNAME record and pointed it to a web server.
- <b>DNS Server Management</b> – Configured and monitored DNS services using Windows Server Manager.
- <b>PowerShell DNS Commands</b> – Executed various commands such as flushdns, ping, & nslookup.

<h2>!!!!!DISCLAIMER!!!!!</h2>

- <b>There was supposed to a screenshot after STEP 9 that showed the process of creating a CNAME called "search."</b>
- <b>This CNAME was also configured to point to the URL of "www.google.com"</b>

<h2>Actions and Observations</h2>

<p> 
<img src="https://imgur.com/2ASqzhP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 1</b> - Attempting To Ping <b>mainframe</b> on <b>CLIENT 1 PC</b>.
<p>
<br />

<p>
<img src="https://imgur.com/uuTOGup.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<b>STEP 2</b> - <b>nslookup mainframe</b> Attempt Fails on <b>CLIENT 1 PC</b>.
<p>
<br />

<p>
<img src="https://imgur.com/wTlivcl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 3</b> - Switching To <b>DC-1 PC</b> To Create a DNS-<b>A Record</b> Named <b>mainframe</b> With <b>DC-1's </b> Private IP Address.
</p>
<br />

<p>
<img src="https://imgur.com/SyYPi6a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 4</b> - Pinged <b>mainframe</b> Succesfully on <b>CLIENT 1 PC</b>.
</p>
<br />

<p>
<img src="https://imgur.com/2cvdip0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 5</b> - Changing <b>mainframe</b> IP Address To <b>8.8.8.8</b> On <b>DC-1 PC</b>.
</p>
<br />

<p>
<img src="https://imgur.com/GkXzhqv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 6</b> - <b>mainframe</b> Still Pinging From <b>10.0.0.4</b> IP Despite IP Address Change.
</p>
<br />


<p>
<img src="https://imgur.com/XqyPjA8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 7</b> - <b>mainframe</b> Still Holds <b>A (Host)</b> 10.0.0.4 When Initiating "ping" Command.
</p>
<br />

<p>
<img src="https://imgur.com/hCFM2av.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 8</b> - Initiated <b>flushdns</b> Command To Get Rid of The Cache on <b>DC-1 PC</b>.
</p>
<br />

<p>
<img src="https://imgur.com/E5AQ6x8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP **9**</b> - The Ping Is Now Showing The New <b>8.8.8.8</b> IP Address.
   
     - Creation of the CNAME "search" Screenshot Was Supposed To Be Here.
</p>
<br />

<p>
<img src="https://imgur.com/2uj185b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 10</b> - Pinged search <b>CNAME</b> search Successfully.
</p>
<br />

<p>
<img src="https://imgur.com/7R0CRWg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>STEP 11</b> - <b>nslookup</b> Results for <b>search</b> CNAME.
</p>
<br />
