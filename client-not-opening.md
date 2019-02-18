---
title: Client Not Opening
layout: post
permalink: /client-not-opening/
---

Before you start troubleshooting, get connected to the client server. Launch Visual Matrix to double-check the error code. Write it down in case your supervisor or team leader asks you for it. 

Write down the server name and IP address, located at the top of the VNClient.

<img src="/portfolio/images/client1.png" alt="client1">

Follow the troubleshooting path below.

## Check the registry

1. In the Windows search bar, type "regedit" then run the regedit command.

2. In the registry editor, follow this folder path in the menu on the left: 

    `:\Hkey_Local_Machine\Software\WOW6432Node\ImageTech\VisualMatrix\Data`

3. Make sure that the info in the Data field next these file names matches this format:

    `file: sharepath_reg_sz` <br>
    `data: "servername"\Vm_Shared`

If the data fields are not formatted like this, or if they have IP addresses where server names should be, speak with your team leader or supervisor.

## Windows Host File

1. In the file explorer, go to:

    `C:\Windows\System32\drivers\etc`
    
2. Right click the **hosts** file and open with Notepad.

    <img src="/portfolio/images/client2.png" alt="client2">

3. Check to see if there is an entry for the server computer's name and IP address. Ideally, there is not an entry.

    <img src="/portfolio/images/client3.png" alt="client3">

4. If there is an entry, validate that they are both correct by comparing them to the server name and IP address at the top of your VNConnect screen.

    - On the server computer: to check the IP and server name another way, open the cmd prompt and type "ipconfig". The IP address is next to the field labelled "Ipv4".
    
## server name

See if you can browse from client to server:

1. Enter `\\'servername'` (with no quotes) in the file explorer.

    - You should be able to see a VM_Shared folder.

    <img src="/portfolio/images/client4.png" alt="client54">

2. Verify that you can view all of the shared folders. 

## Firewall/Antivirus

**DO NOT shut off any of the customer's firewalls/antivirus programs.

1. Give .sql firewall permission. File path:

    `C:\Windows\ProgramFiles(x86)\Microsoft SQL Server\MSSQL10_50.VMATRIX2008\MSSQL\Binn\sqlservr.exe`
    
2. Give **port 1702** firewall permission. 
    - Visual Matrix runs through this port.
    
3. **Temporarily** disable firewall then attempt to open Visual Matrix.

If that does not solve the issue: 

## Get help from supervisor or team lead




