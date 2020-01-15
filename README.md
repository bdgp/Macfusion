Latest Macfusion-NG binary with latest SSHFS binary included
============================================================

One alternative to the macOS SMB shared folders you may want to check out is SSH mounting your directories. It requires a little more set up, but it's more secure than using SMB file sharing and is usable over any server that has SSH installed.

If you want to try it out, go to https://osxfuse.github.io/ and install the "FUSE for macOS" package, then install the "SSHFS" package. After that, extract the ZIP file from the "Releases" page and copy it into your /Applications folder. Then right-click on it and select "Open". 

Then hit the "+" button, and select SSHFS. Enter a name for the connection, then under Host, enter the SSH host. Put your LDAP username in the "User Name" field and your LDAP password. You can set the path to /home/<your username> or another folder. Under the "Macfusion" tab, you need to set the Mount Point to "/Users/<Your user name>/mnt" or some other folder in your home directory that doesn't already exist. Then hit OK to close the window. Now if you click on the "Mount" button, the volume icon should turn green. If you right-click on it, and select "Reveal" from the drop-down, it will pop up your shared home directory files in a Finder window.

For windows users, you have to install sshfs-win: https://github.com/billziss-gh/sshfs-win. Just follow the instructions in the Installation section.
