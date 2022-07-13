PicoCTF Challenge Writeup, Static ain't always noise.
----------------------------------------

**Description:**

Can you look at the data in this binary: [static?](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static) This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!

>No Hints from pico, however...<details>The flag can be discovered plain text on line 35 of static</details>

Firing up our virtual machine, or the web console, lets grab our files.
```` Terminal
$wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
$wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
````
Making the files executable.
```` Terminal
$chmod +x static
$chmod +x ltdis.sh
````

Running static to see what it does.
```` Terminal
$./static
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
````
Cheeky... lets take a look at the bash script

```` Terminal
$cat ltdis.sh
````
The script appears strip text from the assigned program using a strings command, and dumps them to a text file. Awesome, exactly what we need.

```` Terminal
$./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
````

```` Terminal
$cat static.ltdis.strings.txt | grep pico
````

<details>1020 picoCTF{d15a5m_t34s3r_XXXXXXXX} where X's should be a unique number depending on the challenge</details>
