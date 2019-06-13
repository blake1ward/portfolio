## Before starting

Keep these things in mind before you troubleshoot a down server.

* Be sympathetic to the difficult and frustrating situation that the customer is in. This will help us to be more productive and them to be more cooperative.
* The customer needs to understand that this will not likely be a quick and easy issue to resolve. We need to patient to get it fixed.
* Often, a local IT technician is needed to assist. Be sure the customer understands that their IT technician must speak with a Visual Matrix agent before they touch the server. 
* The server is not to be taken offsite, under any circumstance.

The following instructions must be followed in the event that a VM server has gone down.

## Troubleshooting

1. Notify your supervisor. 
   * Your supervisor is here to guide you; they are not taking over your role in the issue.
2. Talk the client through discovering what the problem is, and take descriptive notes. 
   * Ask if the power is coming on. If it is not, the issue may be as simple as replacing a dead power supply.
   * When the power comes on and the server does not boot, is there an error messages? What is the message?
      * "The server is down" is not an acceptable notation. A down server is a big issue, and your notes need to reflect how seriously the issue should be taken.
3. Tell team lead or coordinator to send the hotel a purchase order via Panda Doc. You will need to give them the following information:
   * GM name
   * GM email
   * Property ID
4. Locate an external hard drive that contains secondary backups, if it exists.
   * If you cannot find anything, secondary backups might also be saved on USB drives. Look for them as well.
   * If you still cannot find anything, connect to other client computers on the VM network to see if one of them might have the backups we need.
   * In some cases, it may be acceptable to restore the backup. However, this is **NOT** the ideal solution. Speak to your supervisor.
5. Have the customer look for the backup credit card encryption key.
   * Up until this point, we prefer that the server remains onsite.
6. Have the customer put the server's hard drive in another computer as a secondary drive.
   * The hotel should have an IT professional do this, in most cases.
7. Browse to the drive in Windows explorer.
   * In many cases, the problem is that the Master Boot Record (MBR) on the drive is corrupt. This means that the data is still there, but the drive does not know how to tell the computer where to find the files to boot into Windows.
8. Have a supervisor run a data recovery tool on the drive.
   * In many cases, the Master File Table (MFT) is corrupt, and Windows does not know where to find the files, yet the files exist.
   * A data recovery tool reads all of the sectors of that drive and rebuilds an MFT of its own.
9. Offer the hotel this option: at this point, they can send the drive off to a data recovery specialist.
   * It is expensive.
   * Once we build a new database for them, there is no returning to this lost data.
   * If we create a new database for them, and they are able to eventually recover old data, **it cannot be merged**.
   * Building a new database is an absolute last resort.
10. If steps 7 or 8 work, proceed (under supervision) as determined by what we were able to recover. 
   * If we were able to recover the .mdf and .ldf files then we do not need to resort res or GNR download from Best Western.
   * If we had to restore a backup, we need to request and run a res report, and then request a GNR download from Best Western.
