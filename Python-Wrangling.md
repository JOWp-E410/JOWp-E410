Python Wrangling
----------------
Description

>Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py) using this [password](https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/pw.txt) to get the [flag](https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/flag.txt.en)?

>Hint 1:<details>Get the Python script accessible in your shell by entering the following command in the Terminal prompt: $ wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py</details>

>Hint 2:<details>$ man python</details>

We can use the following command on our virtual machine, or the web console to download the file, alternatively right click and save as.

Python Script 
```` Terminal
$wget https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/ende.py
````
Password
```` Terminal
https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/pw.txt
````
Encrypted Flag
```` Terminal
https://mercury.picoctf.net/static/5c4c0cbfbc149f3b0fc55c26f36ee707/flag.txt.en
````

Looking at the python script it looks like an encoder/decoder system. Running the program in terminal gives us an output:

```` Terminal
$python ende.py
Usage: ende.py (-e/-d) [file]
````

Following along with the description we're going to use the -d flag I assume is short for 'decryption'

```` Terminal
#python ende.py -d flag.txt.en
Please enter the password:192ee2db192ee2db192ee2db192ee2db
````

<details>picoCTF{4p0110_1n_7h3_h0us3_XXXXXXXX} where the X's should be a unique number, depending on the challenge.</details>
