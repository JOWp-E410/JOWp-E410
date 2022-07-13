PicoCTF Challenge Writeup, Wave a Flag.
----------------------------------------

Description
>Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...

>Hint 1:<details>This program will only work in the webshell or another Linux computer.</details>
>Hint 2:<details>To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm</details>
>Hint 3:<details>Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm</details>
>Hint 4:<details>-h and --help are the most common arguments to give to programs to get more information from them!</details>
>Hint 5:<details>Not every program implements help features like -h and --help.</details>

First things first, let's grab the file
```` Terminal
$wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
````
To make it short and sweet we can simply view the flag in plain text on line 27... HOWEVER! Lets run it on our virtual machine or web console just for the sake of it.

Making it Exectuable
```` Terminal
chmod +x warm
````
Running
```` Terminal
./warm
Hello user! Pass me a -h to learn what I can do!
````
Passing the -h
```` Terminal
./warm -h
Oh, help? I actually don't do much, but I do have this flag here:
````
<details>picoCTF{b1scu1ts_4nd_gr4vy_XXXXXXXX} where the X's should be a unique number based on the challenge</details>

Short and sweet, I was immediately dissapointed to have stumbled haphazzardly onto the flag, but oh well.
