# Repair-Win-OS
This is Code to put in the Command Prompt to repair/fix Windows.

Note that you can pick one or more of these to fix your computer, this is not all a step by step, note that it's not my problem if something goes wrong. Please contact microsoft of it gets worse, sorry if this does not help.

#1 Repair Windows 10/11 using SFC:

1. Open "Start", search for the Command Prompt, select it and run as administrator.

2. Then type the command: "sfc /scannow" and press "Enter".
----
#2 Repair Windows 10/11 using DISM:

- To check whether there is any corruption, Run command line as administrator, then type the following syntax and press "Enter".

DISM /Online /Cleanup-Image /CheckHealth

- To scan the Windows image for any corruption, type below command and hit "Enter".

DISM /Online /Cleanup-Image /ScanHealth

- To fix Windows image, type the following command and hit "Enter".

DISM /Online /Cleanup-Image /RestoreHealth /Source:repairSource\install.wim
---
#3 Reset Windows 10/11 with command line:

- Type “systemreset -cleanpc” in an elevated command prompt and press "Enter".  (If your computer cannot boot, you can boot into recovery mode and select "Troubleshoot", and then choose "Reset this PC".)
---- 
#4 Run system restore with command prompt:

1. Start your computer and press "F8" repeatedly until the Windows advanced options menu appears.

2. Click "Safe Mode with command prompt" and press "Enter". If your computer can boot normally, type "cmd" in the search box and click "Command Prompt" to continue.

3. Sign in using an administrator account if needed. Once the command prompt is showing, enter "rstrui.exe" at first in the Command Prompt Window and press "Enter" to continue.
----
#5 Repair Windows 10/11 with AOMEI.exe (Universal):
Go to methid 5 on this site to find out, not that I do not know if this dowload is safe so please consider what your doing. Link: https://www.ubackup.com/windows-10/repair-windows-10-using-command-prompt.html
----
All info pulled from: https://www.ubackup.com/windows-10/repair-windows-10-using-command-prompt.html
