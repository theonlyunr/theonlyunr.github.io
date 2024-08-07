---
title: "The Beginner's Guide to the picoGym"
date: 2024-08-07 00:32:00 +23:55
categories: [CTF]
tags: [CTF]
---
# The Beginner's Guide to the picoGym

## Challenge: Obedient Cat

Author: syreal

### Description

This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).

```powershell
PS D:\Edge Downloads\CTF Tools\CTF\Pico\Sanity> ls

    Directory: D:\Edge Downloads\CTF Tools\CTF\Pico\Sanity

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        07-08-2024     08:21             34 flag

PS D:\Edge Downloads\CTF Tools\CTF\Pico\Sanity> cat .\flag
picoCTF{s4n1ty_v3r1f13d_4a2b35fd}
PS D:\Edge Downloads\CTF Tools\CTF\Pico\Sanity>
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{s4n1ty_v3r1f13d_4a2b35fd}

</aside>

## Reference:

[How to install the Linux Windows Subsystem in Windows 11](https://techcommunity.microsoft.com/t5/windows-11/how-to-install-the-linux-windows-subsystem-in-windows-11/m-p/2701207/page/3)

---

## Challenge: what's a net cat?

Author: Sanjay C/Danny Tunitis

### Description

Using netcat (nc) is going to be pretty important. Can you connect to `jupiter.challenges.picoctf.org` at port `25103` to get the flag?

```powershell
the0nlyunr-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 25103
You're on your way to becoming the net cat master
picoCTF{nEtCat_Mast3ry_d0c64587}

```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{nEtCat_Mast3ry_d0c64587}

</aside>

## Tools: nc

## Reference:

[nc(1): arbitrary TCP/UDP connections/listens - Linux man page](https://linux.die.net/man/1/nc)

---

## Challenge: Mod 26

Author: Pandu

### Description

Cryptography can be easy, do you know what ROT13 is? `cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}`

I used https://gchq.github.io/CyberChef/ and solved it 

![Untitled](The%20Beginner's%20Guide%20to%20the%20picoGym%202a8dde23beab4f35a51d16480cfe1c34/Untitled.png)

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{next_time_I'll_try_2_rounds_of_rot13_hWqFsgzu}

</aside>

## Tools:

[CyberChef](https://gchq.github.io/CyberChef/)

---

## Challenge: Warmed Up

Author: Sanjay C/Danny Tunitis

### Description

What is 0x3D (base 16) in decimal (base 10)?

I just converted base16 to decimal with help of https://www.rapidtables.com/convert/number/hex-to-decimal.html

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoctf{61}

</aside>

## Tools:

[Hex to Decimal Converter](https://www.rapidtables.com/convert/number/hex-to-decimal.html)

## Reference:

**How to identify Base 16 ?**

Base-16 uses 16 values: the numbers 0 to 9 and the letters A to F

---

## Challenge: 2Warm

Author: Sanjay C/Danny Tunitis

### Description

Can you convert the number 42 (base 10) to binary (base 2)?

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoctf{101010}

</aside>

## Tools:

[Hex to Decimal Converter](https://www.rapidtables.com/convert/number/hex-to-decimal.html)

---

## Challenge: Bases

**EasyGeneral SkillspicoCTF 2019**

Author: Sanjay C/Danny T

### Description

What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

[CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9+/=',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE)

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoctf{l3arn_th3_r0p35}

</aside>

## Tools:

[CyberChef](https://gchq.github.io/CyberChef/)

---

## Challenge: Wave a flag

Author: syreal

### Description

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm) has extraordinarily helpful information...

I downloaded the file in terminal with 
1. wget 
2. gave to permission to execute 
3. run the command and got the flag 

```bash
the0nlyunr-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
--2024-08-07 03:33:17--  https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                                   100%[============>]  10.68K  --.-KB/s    in 0s      

2024-08-07 03:33:17 (185 MB/s) - 'warm' saved [10936/10936]
the0nlyunr-picoctf@webshell:~$ chmod +x warm 
the0nlyunr-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
the0nlyunr-picoctf@webshell:~$ ./warm -h 
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
the0nlyunr-picoctf@webshell:~$ 
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}

</aside>

---

## Challenge:Tab, Tab, Attack

Author: syreal

### Description

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/a350754a299cb58988d6d47aed5be3ba/Addadshashanammu.zip)

```bash
 [~/Desktop/CTF/picoctf]
 kali  ls         
Addadshashanammu  Addadshashanammu.zip
               
 [~/Desktop/CTF/picoctf]
 kali  cd Addadshashanammu 
               
 [~/Desktop/CTF/picoctf/Addadshashanammu]
 kali  cd Almurbalarammi  
               
 [~/Desktop/CTF/picoctf/Addadshashanammu/Almurbalarammi]
 kali  cd Ashalmimilkala 
               
 [..top/CTF/picoctf/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
 kali  cd Assurnabitashpi 
               
 [..Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
 kali  cd Maelkashishi   
               
 [..mmu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
 kali  cd Onnissiralis 
               
 [..rammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
 kali  cd Ularradallaku 
               
 [..ilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
 kali  ls              
fang-of-haynekhtnamet
               
 [..ilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
 kali  chmod +x fang-of-haynekhtnamet 
               
 [..ilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
 kali  ls 
fang-of-haynekhtnamet
               
 [..ilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
 kali  ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}
               
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{l3v3l_up!_t4k3_4_r35t!_a00cae70}

</aside>

## Reference:

[tree](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/tree)

---

## Challenge: Insp3ct0r

Author: zaratec/danny

### Description

Kishor Balan tipped us off that the following code may need inspection: `https://jupiter.challenges.picoctf.org/problem/44924/` ([link](https://jupiter.challenges.picoctf.org/problem/44924/)) or http://jupiter.challenges.picoctf.org:44924

`picoCTF{tru3_d3`  I found this on Source code , 3rd part is in java code `flag: _lucky?f10be399}`and the second path is in CSS `t3ct1ve_0r_ju5t` 

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?f10be399}

</aside>

---

## Challenge: strings it

Author: Sanjay C/Danny Tunitis

### Description

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?
I did strings and grep because they where many strings 

```bash
[~/Desktop/CTF/picoctf]
kali  strings strings | grep pico
picoCTF{5tRIng5_1T_d66c7bb7}
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{5tRIng5_1T_d66c7bb7}

</aside>

---

## Challenge: First Grep

Author: Alex Fulton/Danny Tunitis

### Description

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.

Same challenge as above:

```bash
 [~/Desktop/CTF/picoctf]
 kali  strings file | grep pico        
picoCTF{grep_is_good_to_find_things_f77e0797}
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{grep_is_good_to_find_things_f77e0797}

</aside>

---

## Challenge: where are the robots

Author: zaratec/Danny

### Description

Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/60915/` ([link](https://jupiter.challenges.picoctf.org/problem/60915/)) or http://jupiter.challenges.picoctf.org:60915

I navigated to [https://jupiter.challenges.picoctf.org/problem/60915/robots.txt](https://jupiter.challenges.picoctf.org/problem/60915/robots.txt) and found 

```
User-agent: *
Disallow: /8028f.html
```

when I went to [https://jupiter.challenges.picoctf.org/problem/60915/8028f.html](https://jupiter.challenges.picoctf.org/problem/60915/8028f.html) I got the flag. 

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{ca1cu1at1ng_Mach1n3s_8028f}

</aside>

---

## Challenge: Python Wrangling

Author: syreal

### Description

Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/ende.py) using [this password](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/pw.txt) to get [the flag](https://mercury.picoctf.net/static/2ac2139344d2e734d5d638ac928f1a8d/flag.txt.en)?

I used wget to get all the files and then I used `-d` to attack the flag file then  I have entered 

```bash

kali  cat pw.txt      
68f88f9368f88f9368f88f9368f88f93
               
 [~/Desktop/CTF/picoctf]
 kali  python3 ende.py -d flag.txt.en 
Please enter the password:68f88f9368f88f9368f88f9368f88f93
picoCTF{4p0110_1n_7h3_h0us3_68f88f93}
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{4p0110_1n_7h3_h0us3_68f88f93}

</aside>

## Tools: python

## Reference:

[CTFtime.org / picoCTF 2021 / Python Wrangling / Writeup](https://ctftime.org/writeup/28149)

---

## Challenge: PW Crack 1

Author: LT 'syreal' Jones

### Description

Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too [here](https://artifacts.picoctf.net/c/11/level1.py) [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc).

I have downloaded the code and if we go through the code we will find the password as `1e1a` 

```bash
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level1.flag.txt.enc', 'rb').read()

def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

level_1_pw_check()

```

After getting to know the password then I run the same command  `python3 level1.py -d level1.flag.txt.enc`  and then used the password from above got the flag 

```bash
 [~/Desktop/CTF/picoctf/python]
 kali  python3 level1.py -d level1.flag.txt.enc 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{545h_r1ng1ng_fa343060}

</aside>

---

## Challenge: PW Crack 2

Author: LT 'syreal' Jones

### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too. [here](https://artifacts.picoctf.net/c/13/level2.py) [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc)

```bash
f str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()

def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

level_2_pw_check()
```

If we observe form the above code we need to decode `chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36).`  we get the password as `de76`  after that if we run 

`python3 level2.py -d level2.flag.txt.enc` and enter de76 we get the flag. 

```bash
[~/Desktop/CTF/picoctf/python2]
 kali  python3 level2.py -d level2.flag.txt.enc
Please enter correct password for flag: de76 
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{tr45h_51ng1ng_489dea9a}

</aside>

---

## Challenge: PW Crack 3

Author: LT 'syreal' Jones

### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.[here](https://artifacts.picoctf.net/c/17/level3.py) [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin)

```bash
# The
00000498  73 74 72 69 6E 67 73 20 62 65 6C 6F 77 20 61 72 65 20 37 20 70 6F 73 73 69 62 69 6C 69 74 69 65 73 20 66 6F 72 20 74 68 65 20 63 6F 72 72 65 63 74 20 70 61 73 73 77 6F strings below are 7 possibilities for the correct passwo
000004D0  72 64 2E 20 0D 0A 23 20 20 20 28 4F 6E 6C 79 20 31 20 69 73 20 63 6F 72 72 65 63 74 29 0D 0A 70 6F 73 5F 70 77 5F 6C 69 73 74 20 3D 20 5B 22 66 30 39 65 22 2C 20 22 34 rd. ..#   (Only 1 is correct)..pos_pw_list = ["f09e", "4
00000508  64 63 66 22 2C 20 22 38 37 61 62 22 2C 20 22 64 62 61 38 22 2C 20 22 37 35 32 65 22 2C 20 22 33 39 36 31 22 2C 20 22 66 31 35 39 22 5D 0D 0A 0D 0A                      dcf", "87ab", "dba8", "752e", "3961", "f159"]....

```

The correct answer is in  `["f09e", "400000508  64 63 66 22 2C 20 22 38 37 61 62 22 2C 20 22 64 62 61 38 22 2C 20 22 37 35 32 65 22 2C 20 22 33 39 36 31 22 2C 20 22 66 31 35 39 22 5D 0D 0A 0D 0A                      dcf", "87ab", "dba8", "752e", "3961", "f159"]`. So I decided to try all the passwords and the correct one is `87ab.` 

```bash
[~/Desktop/CTF/picoctf/python3]
 kali  python3 level3.py -d level3.flag.txt.enc
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

*PS: It is not the ideal way* 

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{m45h_fl1ng1ng_cd6ed2eb}

</aside>

## Tools: bvi

A cmd tool to see the hex and binary 

## Reference:

[https://bvi.sourceforge.net/install.html#:~:text=The Unix version of bvi,ncurses](https://bvi.sourceforge.net/install.html#:~:text=The%20Unix%20version%20of%20bvi,ncurses) 

---

## Challenge: PW Crack 4

Author: LT 'syreal' Jones

### Description

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/21/level4.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/21/level4.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/21/level4.hash.bin) in the same directory too.There are 100 potential passwords with only 1 being correct. You can find these by examining the password checker script. 

The give python code me 

```python
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level4.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level4.hash.bin', 'rb').read()

def hash_pw(pw_str):
    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()

def level_4_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)
    
    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

level_4_pw_check()

# The strings below are 100 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8c86", "7692", "a519", "3e61", "7dd6", "8919", "aaea", "f34b", "d9a2", "39f7", "626b", "dc78", "2a98>

```

In  the modification what I did is I added a for loop to check everything form `pos_pw_list` 

```python
for  pw  in  pos_pw_list :
         level_4_pw_check(pw)
```

If I just run the code I got the flag 

```bash
python level4m.py
Welcome back... your flag, user:
picoCTF{fl45h_5pr1ng1ng_d770d48c}
```

<aside>
<img src="https://www.notion.so/icons/flag-swallowtail_green.svg" alt="https://www.notion.so/icons/flag-swallowtail_green.svg" width="40px" /> picoCTF{fl45h_5pr1ng1ng_d770d48c}

</aside>

## Reference:

[PicoCTF Walkthru [66] - PW Crack 4 (PW Hashing)](https://www.youtube.com/watch?v=yiKJdVG6R3U)

---

---