# NahamCon_2021_CTF

- [Warmups](#warmups)
  * [Veebee](#veebee)
  * [Read The Rules](#read-the-rules)
  * [Chicken Wings](#chicken-wings)
  * [Car Keys](#car-keys)
  * [Buzz](#buzz)
  * [Pollex](#pollex)
  * [Shoelaces](#shoelaces)
  * [esab64](#esab64)
  * [Eighth Circle](#eighth-circle)
- [Web](#web)
  * [Homeward Bound](#homeward-bound)
  * [$Echo](#$Echo)
  * [Cereal and Milk](#cereal-and-milk)
  * [AgentTester](#agenttester)
  * [Asserted](#asserted)
  * [AgentTester V2](#agenttester-v2)
- [Binary Exploitation](#binary-exploitation)
  * [Ret2basic](#ret2basic)
- [Cryptography](#cryptography)
  * [Treasure](#treasure)
  * [eaxy](#eaxy)
  * [Dice Roll](#dice-roll)
- [Forensics](#forensics)
  * [Parseltongue](#parseltongue)
  * [Henpeck](#henpeck)
- [Mobile](#mobile)
  * [Andra](#andra)
  * [Resourceful](#resourceful)
  * [Microscopium](#microscopium)
- [Miscellaneous](#miscellaneous)
  * [Abyss](#abyss)
  * [Prison Break](#prison-break)
- [Scripting](#scripting)
  * [DDR](#ddr)
- [Mission](#mission)
  * [Gus](#gus)
  * [Lyra](#lyra)
  * [Hercules](#hercules)
  * [Orion](#orion)
  * [Leo](#leo)
  * [Internal](#internal)
  * [Rotten Logging](#rotten-logging)
  * [Banking on it](#banking-on-it)
  * [Degrade](#degrade)
  * [Meet The Team](#meet-the-team)
  * [Bionic](#bionic)
  * [The Mission](#the-mission)
  * [Hydraulic](#hydraulic)
  * [Backdoor](#backdoor)
- [Sponsors Recon](#sponsors-recon)
  * [Google Play](#google-play)
  * [Intigriti](#intigriti)
  * [INE (Starter Pass)](#ine--starter-pass-)
  * [HackerOne](#hackerone)
- [HackTheBox Academy](#hackthebox-academy)
  * [HTB Module - Attacking Web Applications with Ffuf](#htb-module---attacking-web-applications-with-ffuf)
  * [HTB Challenge - Weather App](#htb-challenge---weather-app)
  * [HTB Challenge - Weather App](#htb-challenge---weather-app-1)




## Warmups

### Veebee

`Buzz buzz, can you find the honey?`

From the title of the challenge, I assumed that it was visual basic, so I renamed it to vbs, tried to run it, it failed. I googled Visual Basic file extensions and found .vbe, I ran it and it went through some popups until the flag appeared

![](/images/veebee.png)

Flag: `flag{f805593d933f5433f2a04f082f400d8c}`

### Read The Rules





### Chicken Wings





### Car Keys





### Buzz





### Pollex





### Shoelaces





### esab64





### Eighth Circle





## Web

### Homeward Bound





### $Echo

`So I just made a` ~~hardcoded~~ `bot that basically tells you what you wanna hear. Now usually it's a $ for each thing you want it to say but I'll waive the fee for you if you beta test it for me.`	


$Echo was an easy web challenge that ended up at 50 points.
	We are presented with a text box that takes input, and uses the `echo` program to return our input. After trying to find command injection, we see that the only allowed special characters are \` and <./
There was also a 15 character limit on input. After some research, i found that commands inside backticks would be executed, and the response returned.
\`ls\` gave us the `index.php`, and \`ls .\.\` returned a `flag.txt`

Due to the 15 character limit, it was impossible for us to use the cat command (e.g. \`cat .\.\flag.txt`) so we had to find another way of reading the file. After research, i found that the < character could send input to stdout. This allowed the crafting of the final payload:

\`< .\.\/flag.txt`
which returned us a flag. 

`

### Cereal and Milk





### AgentTester





### Asserted





### AgentTester V2

## Binary Exploitation

### Ret2basic





## Cryptography

### Treasure

`This movie is what pushed me to get into hacking. Good luck decrypting my note, I'm elite.`

There are two files provided with the question: `notes.txt` and `hackers.txt`

`note.txt` is a text document with a flag in a 4 digit numerical format

`hackers.txt` is the script for the movie Hackers

I thought it would be similar to a book cipher so I googled a book cipher decoder and clicked on the first link: [decode.fr/book-cipher](https://www.dcode.fr/book-cipher) I input the data into it and it returned the flag

![](/images/hackers.png)

Flag: `flag{62D869C6B886DAC2DD743086E451F76B}`

### eaxy





### Dice Roll





## Forensics

### Parseltongue





### Henpeck





## Mobile

### Andra





### Resourceful





### Microscopium





## Miscellaneous

### Abyss





### Prison Break





## Scripting

### DDR





## Mission

### Gus





### Lyra





### Hercules





### Orion





### Leo





### Internal





### Rotten Logging





### Banking on it





### Degrade





### Meet The Team





### Bionic





### The Mission





### Hydraulic





### Backdoor

## Sponsors Recon

### Google Play





### Intigriti 





### INE (Starter Pass)





### HackerOne





## HackTheBox Academy

### HTB Module - Attacking Web Applications with Ffuf





### HTB Challenge - Weather App





### HTB Challenge - Weather App





### HTP Module - Linux Fundamentals





### HTB Module - Introduction to Web Applications





### HTB Challenge - LoveTok

## NahamCon

### INE Career Corner





### IoT Village





### Live Recon Village





### Red Team Village





### UHC-BR





### #NahamCon2021





### Merch Store



