---
title: Encryption Key Backup
layout: post
permalink: /encryption/
---


When a hotel is having a issue with their encryption keys, their call will most likely start with: "I can't see credit card numbers."

* The error is: "Encryption Key Mismatch!"
* To verify that this is the issue, try pulling up a reservation that had used a credit card. If the encryption keys are mismatched, the numbers will be X'd out (XXXX-XXXX-XXXX-XXXX)

Perform the following troubleshooting pattern on the server computer.

## Check for the USB drive in file explorer

Sometimes the USB drive is not visible, or the USB drive has not been properly inserted into the computer.

1. Open the file explorer, looking for the USB drive.

2. If the drive is not visible, ask the customer to find the drive and plug it in. If it is already plugged in, ask the customer to unplug the drive. Wait a couple of seconds and plug the drive back in.

3. If you cannot see the drive, ask the customer to find and insert one of the backup encryption keys.

* If no keys appear on the server computer, get connected to the client computer and have them insert the drives on that computer. If they do now show on the client computer, talk to a team leader or supervisor.

4. If you can see the USB drive, double-click and open the drive. There should be a file named IT_VM_KEY.DAT, check the size of the files. If you can see the USB drive, double-click and open the drive.

* The active key is always 1 kB.
* The backup keys are always 4 kB.

5. If the key is now visible: restart the device server and log out of Visual Matrix. Once the device server is restarted, log back into Visual Matrix. Do you get a mismatch error? If so, the next step is to restore a key to the keystore; they will need a backup encryption key for this step..

## Restore key to keystore

**Note**: If the hotel has an active key but no backup keys, skip this section.

1. Launch ImportDB.exe, in the folder Devices folder:

`C:\ImageTech\VisualMatrix\Devices\ImportDB.exe`

**How to use ImportDB**

There are different ways to click the Delete Key Store button:
* Click = Delete the key from keystore
* CTRL + Click = Creates a backup key from the active key
* ALT + Click = Restores key to keystore

2. Use ALT + Click on **Delete Key Store** to restore the keystore.

3. Restart the device server, log out and log back into Visual Matrix, and see if restoring the keys fixed the issue.

## Create new backup key (must have an active key)

**Note**: When you do a server reinstall, it is often necessary to create a new backup key.

1. Open **importdb.exe** (if doing a server reinstall, this takes place on the old server).

2. Use CTRL + Click on the **Delete Key Store** button to create a backup key.

   * When you create a backup key, it is dumped on the C: drive. 

3. Locate the new backup key and move it to the external drive. The hotel needs to provide an empty USB drive for the new backup.

   * If you are using the same drive that the active key is on, you will need to temporarily rename the active key.
      * Add a "1" or any similar text to the name that you will be able to easily remove.

4. Restore the key to the key store (refer to the second section of this article).

<hr>

If you are unable to resolve the issue, speak to a floor lead or supervisor.
