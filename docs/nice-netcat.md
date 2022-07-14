PicoCTF Challenge Writeup, Nice Netcat...
----------------------------------------

**Description:**

There is a nice program that you can talk to by using this command in a shell: $ 'nc mercury.picoctf.net 7449', but it doesn't speak English...

>Hint 1:<details>You can practice using netcat with this picoGym problem: [what's a netcat?](https://play.picoctf.org/practice/challenge/34)</details>
>Hint 2:<details>You can practice reading and writing ASCII with this picoGym problem: [Let's Warm Up](https://play.picoctf.org/practice/challenge/22)</details>

From the netcat manual (man nc) 
>The nc (or netcat) utility is used for just about anything under the sun involving TCP, UDP, or UNIX-domain sockets.  It can open TCP connections, send UDP packets, listen on arbitrary TCP and UDP ports, do port scanning, and deal with both IPv4 and IPv6.  Unlike telnet, nc scripts nicely, and separates error messages onto standard error instead of sending them to standard output, as telnet does with some.

Connecting to the server:
```` Terminal
$nc mercury.picoctf.net 7449 (your port may be different)
````
We are met with a series of numbers.

>112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 88 88 88 88 88 88 88 88 125 10 

This challenge is about basic skills, so I'm guessing that it's not excryption or cypher it's likely ASCII, quick peak at the hint confirms this. Tools found [here](https://www.prepostseo.com/tool/ascii-to-text), or here [ddg Search](https://duckduckgo.com/?q=ascii+translator&t=newext&atb=v324-1&ia=web) will translate this for us automatically. Or alternatively we can look up the ASCII codes to text and do it by hand [ASCII table](https://en.wikipedia.org/wiki/File:ASCII-Table.svg).

By Hand
><details>p i c o C T F { g 0 0 d _ k 1 t t y ! _ n 1 c 3 _ k 1 t t y ! _ X X X X X X X X }</details>
Spaces removed
><details>picoCTF{g00d_k1tty!_n1c3_k1tty!_XXXXXXXX} where the X's should be a unique number for you depending on the challenge.</details>

Again a quick and fun ctf.
