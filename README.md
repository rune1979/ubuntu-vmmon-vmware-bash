# ubuntu-vmmon-vmware-bash
<p>Simpel bash script for updating MOK keys for VMWare in Ubuntu (and probably other Debian based distrobutions): Typical error occurs when attempting to boot virtual machine in VMWare <b>"Cannot open /dev/vmmon: No such file or directory"</b>.</p><p> Why automate this process? You may ask. In my case I don't want to make a complete reinstall and I'm not even sure it will work. And every time I patch my Debian based system it seems like the MOK keys loss their privileges.</p><p> After this setup I just open the terminal and execute the following command (<b>./wm_autoupdate_key.sh</b>) in the terminal, when VMWare complain about "vmmon"</p> 
<p>
<b>Step 1:</b> Open your terminal en paste the following command (it will get the bash script to your current dir)<br>
$ wget https://raw.githubusercontent.com/rune1979/ubuntu-vmmon-vmware-bash/master/wm_autoupdate_key.sh
<br><br>
<b>Step 2:</b> Make the file executable<br> 
$ sudo chmod +x wm_autoupdate_key.sh
<br><br>
<b>Step 3:</b> Execute the script<br>
$ ./wm_autoupdate_key.sh
</p>
<p>If everything seems to work out successfully. You should now ($ reboot) your machine and choose "Enroll MOK" in the blue menu and follow the instructions and reboot. After that your VMWare should be up and running again.</p>
<p>
  <b>Next time:</b> you have patched your OS, just navigate to the script folder in your terminal and execute the script:<br>
  $ ./wm_autoupdate_key.sh
</p>
