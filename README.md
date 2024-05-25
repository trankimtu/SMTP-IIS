# SMTP-IIS

## Install Web Server IIS and SMTP
From Windows Server Management
<ul>
  <li>Manage</li>
  <li>Add Roles and Features</li>
  <li>Before you begin: Next</li>
  <li>
    Select installation type:
    <ul>
      <li>Role-based or feature-based installation</li>
      <li>Next</li>
    </ul>
  </li>
  <li>Select a server from the server pool: Next</li>
  <li>
    Select server roles
    <ul>
      <li>Select Web Server (IIS)</li>
      <li>Add Features</li>
      <li>Next</li>
    </ul>
    
  </li>
  <li>
    Select features
    <ul>
      <li>Select SMTP Server</li>
      <li>Add Features</li>
      <li>Next</li>
    </ul>
  </li>
  <li>Install</li>
</ul>

## Reset IIS
Run cmd as administrator and powershell as administrator
```
iisreset
```


## Configure SMTP
Open Internet Information Services (IIS) 6.0 Manager

From Server Manager
<ul>
  <li>Tools</li>
  <li>Internet Information Services (IIS) 6.0 Manager</li>
</ul>


Rightclick on [SMTP Virtual Server #1] --> Start

Rightclick on [SMTP Virtual Server #1] --> Property

mmc has detected an arror in a snap-in
Open "run"
```
mmc
file
Add/Remove Snap-in...
Select "Internet Information Services (IIS) 6.0 Manager
Add
OK
```
From console, open SMTP property<br>
Open console, remove IIS 6.0 Manager <br>
Now go back to IIS 6.0 Manager, open property <br>

or

```
Stop SMTPSVC [Display name: Simple Mail Transfer Protocol (SMTP)]
Stop IISADMIN [Display name: IIS Admin Service]
Edit "C:\Windows\System32\inetsrv\MetaBase.xml"
Find: <IIsSmtpServer Location="/LM/SmtpSvc/1"
Add (Settings are alphabetical): RelayIpList=""
Save File
Start the IISAdmin service
Start the SMTPSVC service
```

From (SMTP) Virtual Server #1) Properties





Port 25: Standard SMTP port for server-to-server communication. Used for relaying emails between mail servers.

Port 587: Submission port for email clients to submit outgoing mail to a mail server. Often used with STARTTLS for encryption. This port is commonly used for authenticated SMTP submission by mail clients.

Check port 25 is listening:
netstat -a -n | find "25"

C:\inetpub\mailroot
