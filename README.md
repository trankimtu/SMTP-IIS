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
Run cmd as administrator
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


Right click on [SMTP Virtual Server #1] --> Start


  
