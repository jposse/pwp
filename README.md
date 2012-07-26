pwp
===

Password Paste: A simple bash based password management system

What does it do for me?
=======================
		

		Simply put, it allows you to quickly enter and retrieve passwords. When it retrieves a password 
		it automatically puts it in the clipboard buffer for 30 secs so you can simply paste it where you need. 

		After 30 secs your clipboard buffer will be restored to whatever information it originally contained. 

		Your password file is stored at: ~/.pwp/pwp.asc.gpg

		Although this uses gpg to secure your files it should be noted that this utility IS NOT RECOMMENDED FOR USE
		ON MULTI-USER SYSTEMS!

		This is a simple utility, not intended to be a complete solution.  

Features:
==========
		Works on linux / mac / solaris
		Simple operation
		Just a bash script: you can easily verify not doing anything shady with your information 
		

Requirements: 
=============
		gpg / gpg2
		bash / posix system (specifically, you will need: read, head, cut, tr, printf, /dev/urandom, awk)
		vi
		some form of command-line clipboard management tools (xclip linux / pbpaste pbcopy on mac) 
Example usage:
==============
		

		Create a new entry
		===================
		$pwp set google
		Enter username: joe@gmail.com
		Enter password or leave blank for random: ******

	
		Get existing entry
		===================
		$pwp get google
		Enter username (or leave blank): joe@gmail.com
		Password is in buffer for 30 seconds.....
		(30 secs later)
		Buffer reset


		List all entries (no passwords shown)
		===================
		$pwp list

		Edit the entries directly
		=========================
		$pwp edit

		Configure defaults
		===================
		$pwp config

Installation Instructions
=========================
		
		1. Download pwp file
		2. Put somewhere in your search path (ie. /usr/local/bin or /home/youruser/bin)
		3. Mark pwp file as executable (eg. chmod u+x pwp)
		4. Configure pwp (eg. pwp config)
		5. Add entries (either by "pwp set" or directly via "pwp edit")
		6. Test by using "pwp get" on one of your entries and see if it works correctly with clipboard

Credits
========

		Original idea by tr0lltherapy of reddit. See thread here: 

		http://www.reddit.com/r/programming/comments/x0nzz/very_simple_nononsense_password_manager_that_uses/c5i7ekn


