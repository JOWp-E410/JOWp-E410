PicoCTF Challenge Writeup, Obedient Cat.
----------------------------------------

**Description:**

>This file has a flag in plain sight (aka "in-the-clear"). Download [flag](https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag)

>Hint 1:<details>Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.</details>

>Hint 2:<details>To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag</details>

>Hint 3:<details>$man cat (gives us the manual for the 'cat' command.)</details>

We know the file is hidden in plain sight given the description of our challenge.

From our terminal we can use wget to download the flag to our virtual machine, or using the picoCTF console, run the command:

```` terminal
$wget https://mercury.picoctf.net/static/704f877da185904ec3992e7255a15c6c/flag
````
Then we can simply look at the file. Clue 3 has a hint at how to use 'cat.' It is however rather straightforward in this instance.

```` terminal
$cat flag
````

This returns:

<details>
picoCTF{s4n1ty_v3r1f13d_XXXXXXXX} Note: The X's should be a unique code for you, but this can vary depending on the challenge.
</details>

Alternatively, you can simply download the file and open it with any text editor providing the same results, where's the fun in that?

#obedientcat #picoctf #generalskills
