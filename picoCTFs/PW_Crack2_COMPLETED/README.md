-----------------------------------------
			   PW_Crack2 
-----------------------------------------

###### SOLVED at the first_stage #######

```````````````````````````````````````````````````````````````
```````````````````````````````````````````````````````````````
						Solving Phase
```````````````````````````````````````````````````````````````
```````````````````````````````````````````````````````````````

at first i read the code to understand what is going on inside it
after reading and understanding it

i run the code and saw a error of file opening for the flag :--->

		Traceback (most recent call last):
  			File "/home/rabindra/Desktop/picoCTF/PW_Crack2/first_stage.py", line 12, in <module>
    	flag_enc = open('level2.flag.txt.enc', 'rb').read()
		FileNotFoundError: [Errno 2] No such file or directory: 'level2.flag.txt.enc'

so added the full path of the flag file in the code and it ran without any error, but it was asking for the password.. now i used a little trick to ditermine the password..

and that is: -->
	run python in the terminal of kali and copy and past the password check code which i got from the code in it.. 
	and the password check code is -->

		chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65)

		passwd= 39ce

and the flag is :-->
	picoCTF{tr45h_51ng1ng_502ec42e}




