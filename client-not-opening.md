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

`file: sharepath_reg_sz
data: "servername"\Vm_Shared     <-the server name in the actual file does not have quotes`

