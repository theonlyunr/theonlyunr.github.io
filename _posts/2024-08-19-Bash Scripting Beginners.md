---
title: "Bash Scripting Beginners"
date: 2024-08-19 00:40:00 +23:55
categories: [THEORY]
tags: [SCRIPTING]
---
# Bash Scripting Beginners

We will be using WSL to learn bash scripting. 

1. `echo Hello world!` will print Hello world!
2. `cat <file.txt>` will open the content of the file 

## Basics:

Learning `vim`is important:

1. `vim [file.sh](http://file.sh)` will open vim 
2. Enter `i` to see insert into the file else use **append `a`** insert after the curser. 
3. hit `esc` and come to command mode and then enter `:wq` to write and quit the file. 
4. use `:q!` to come without updating anything and quit. 
5. Run the script with `bash <script name>`

### My first bash Script:

1. Open `vim` and after that hit `i` and then enter the script i.e `echo hello world` and after entering hit `esc` and hit `:wq` 
2. Run the script with `bash hello.sh`

```bash
unr@UNRLAPTOP:~/Desktop/Bash$ cat hello.sh
echo Hello World
unr@UNRLAPTOP:~/Desktop/Bash$ bash hello.sh
Hello World
```

<aside>
💡 echo $SHELL

</aside>

The above command will tell what shell we are running. Ours is `/bin/bash`  we can tell this in the script also. 

```bash
#!/bin/bash 
echo hello world 
```

1. To run the script without tell the `bash` is we need to add `#!/bin/bash`  in script. 
2. Then we need to give `chmod u+x [hello.sh](http://hello.sh/)` to give user the execute the script with `./<script_name>`

---

## Variables:

Assign values to names for reuse within shell scripts and commands.

Example:

```bash
#!/bin/bash

FIRST_NAME=the_only
LAST_NAME=unr

echo Hello $FIRST_NAME $LAST_NAME

```

**Rules to define variables:**

1. When defining their should be no space between variables 

<aside>
<img src="https://www.notion.so/icons/checkmark-line_green.svg" alt="https://www.notion.so/icons/checkmark-line_green.svg" width="40px" /> Variable_Name=Value —> No space

</aside>

<aside>
🚫 Variable_Name =Value —> Giving space

</aside>

1. When calling variables we need to use `$Variable_Name`  

### Taking input form user:

We will use `read`  function we take input form the user. 

```bash
#!/bin/bash

echo Enter your first name:
read FIRST_NAME
echo ENter your last name:
read LAST_NAME
echo Hello $FIRST_NAME $LAST_NAME
```

---

## Positional Arguments

Arguments are a specific positions 

Commands Can take in arguments at a specific position 

```bash
#!/bin/bash

echo Hello $1 $2
```

In this user gives variables in `$1` and `$2` when exciting the function as bellow 

---

## I/O Redirection

- **`<` (Single less-than):** Used to redirect input from a file to a command, as in `command < file`.
- **`<<` (Here document):** Used to redirect a block of text as input to a command, ending the input when a specific delimiter is encountered, as in `command << EOF`.
- **`<<<` (Here string):** Used to redirect a string as input to a command, as in `command <<< "input string"`.

---

## Test Operator

---

## IF/ELIF/ELSE

<aside>
⚠️ , , is used to ignore the case sensitivity

</aside>

Example code:

```bash
#!/bin/bash

if [ ${1,,} = unr ]; then
        echo "hello caption $1"
elif [ ${1,,} = help ]; then
        echo "Enter the username"
else
        echo "Who the Fu*k are you ?"
fi
```

Keep in mind:

1. Keep `;` after the condition  
2. Use `" "` for the echo statements 
3. `fi` is used to close the `if/elif/else`block and `,,` is used ignore case sensitivity. 

---

## Case Statement

```bash
#!/bin/bash

case ${1,,} in
        unr | root)
                echo "Hello Boss $1";;
        help)
                echo "Enter the username";;
        *)
                echo "Invalid username";;
esac
```

Keep in mind:

1. We can use `|` to give multiple options 
2. We need to close the  option with `;;`
3. `esac` is used to end the case statement and `*` is used to all other options 

---

## Arrays:

1. `$ MY_LIST=(unr dd mani krishna avi)` this is how me define out array the `Variable=(value 1 Value 2)`note that we need to give `space` in between the values and `no space`between array name and values. 
2. To print the values we use `echo ${List_Name[@]}` to print all the variables.

```bash
unr@UNRLAPTOP:~/Desktop/Bash$ MY_LIST=(unr dd mani krishna avi)
unr@UNRLAPTOP:~/Desktop/Bash$ echo $MY_LIST
unr
unr@UNRLAPTOP:~/Desktop/Bash$ echo ${MY_LIST[@]}
unr dd mani krishna avi
unr@UNRLAPTOP:~/Desktop/Bash$ echo ${MY_LIST[0]}
unr
```

---

## Loops

syntax

```bash
#!/bin/bash

for variable in list
do
    # commands to be executed
done
```

Example:

```bash
#!/bin/bash

for i in {1..5}
do
    echo "Iteration $i"
done
```

---

## Function

The basic syntax is

```bash
function_name() {
    # commands to be executed
}
```

This is how  a function is defined 

```bash
#!/bin/bash

greet() {
    echo "Hello, $1!"
}

greet "World"
```

**Output:**  In this example, the function `greet` is defined, which takes one argument and prints a greeting. When the function is called with `"World"` as the argument, it prints "Hello, World!".

```bash
#!/bin/bash
showtime(){
        up=$(uptime -p | cut -c4-)
        since=$(uptime -s)
        cat << EOF
----------------------------------
This machine has been up for ${up}
It has been running since ${since}
-----
EOF
}
showtime
```

Output:

```bash
$ ./function.sh
----------------------------------
This machine has been up for 1 hour, 34 minutes
It has been running since 2024-08-19 13:25:50
-----
```

---

## AWK

AWK is a **powerful text-processing programming language** used primarily for pattern scanning and processing.

```bash
Usage: awk [POSIX or GNU style options] -f progfile [--] file ...
Usage: awk [POSIX or GNU style options] [--] 'program' file ...
POSIX options:          GNU long options: (standard)
        -f progfile             --file=progfile
        -F fs                   --field-separator=fs
        -v var=val              --assign=var=val
Short options:          GNU long options: (extensions)
        -b                      --characters-as-bytes
        -c                      --traditional
        -C                      --copyright
        -d[file]                --dump-variables[=file]
        -D[file]                --debug[=file]
        -e 'program-text'       --source='program-text'
        -E file                 --exec=file
        -g                      --gen-pot
        -h                      --help
        -i includefile          --include=includefile
        -l library              --load=library
        -L[fatal|invalid|no-ext]        --lint[=fatal|invalid|no-ext]
        -M                      --bignum
        -N                      --use-lc-numeric
        -n                      --non-decimal-data
        -o[file]                --pretty-print[=file]
        -O                      --optimize
        -p[file]                --profile[=file]
        -P                      --posix
        -r                      --re-interval
        -s                      --no-optimize
        -S                      --sandbox
        -t                      --lint-old
        -V                      --version

To report bugs, see node `Bugs' in `gawk.info'
which is section `Reporting Problems and Bugs' in the
printed version.  This same information may be found at
https://www.gnu.org/software/gawk/manual/html_node/Bugs.html.
PLEASE do NOT try to report bugs by posting in comp.lang.awk,
or by using a web forum such as Stack Overflow.

gawk is a pattern scanning and processing language.
By default it reads standard input and writes standard output.

Examples:
        awk '{ sum += $1 }; END { print sum }' file
        awk -F: '{ print $1 }' /etc/passwd
```

### Resources

[Bash Scripting Tutorial for Beginners](https://youtu.be/tK9Oc6AEnR4?si=5YLLC90qH4A7-oCR)