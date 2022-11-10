```````````````````````````````
          Corridor
     IP= 10.10.233.161
 DATE = 21/10/22 (dd/mm/yyyy)
```````````````````````````````
-------------------------------------

_____________________________________
STEPS:- 
-------------------------------------

so, there is 13 doors....

if i navigate mouse over the doors and click to visit the page, it gives me a hash in the url and also in the mouse fill handle ..

then i tried to copy those hashes from the source code and tried to decode the hashes and got this -->

hashes & dehashes of the door :-

		c4ca4238a0b923820dcc509a6f75849b --> 1
		c81e728d9d4c2f636f067f89cc14862c --> 2
		eccbc87e4b5ce2fe28308fd9f2a7baf3 --> 3
		a87ff679a2f3e71d9181a67b7542122c --> 4
		e4da3b7fbbce2345d7772b0674a318d5 --> 5
		1679091c5a880faf6fb5e6087eb1b2dc --> 6
		8f14e45fceea167a5a36dedd4bea2543 --> 7
		c9f0f895fb98ab9159f51fd0297e236d --> 8
		45c48cce2e2d7fbdea1afc51c7c6ad26 --> 9
		d3d9446802a44259755d38e6d163e820 --> 10
		6512bd43d9caa6e02c990b0a82652dca --> 11
		c20ad4d76fe97759aa27a0c99bff6710 --> 12
		c51ce410c124a10e0db5e4b97fc2af39 --> 13

but i noticed a twist,,,

if i came to this corridor that means there should be a another door behind me if i am facing towards the mid door which is 7th hash....

and that door should be 0th door/hash, so i tried to hash the 0 with this command in the terminal -->  

		echo -n "0" | md5sum

hash of 0 is -->
-------------------

	cfcd208495d565ef66e7dff9f98764da --> 0

and navigate to the page:-
------------------------------

FLAGS
~~~~~~~~

1) what is the flag? 

-->  flag{2477ef02#####9156661ac40a#######} 
~~~~~~~~