# 1. Hello Hackers

## Intro to commands
In this challenge, you will invoke your first command! When you type a command and hit enter, the command will be invoked, as so:

### Solve
**Flag:** `pwn.college{0A-buwr6cYY7R__wLw0nmbzsyUR.QX3YjM1wCMxYzNyEzW}`

I typed hello.

```bash
hello 
pwn.college{0A-buwr6cYY7R__wLw0nmbzsyUR.QX3YjM1wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## Intro to arguments
Let's try something more complicated: a command with arguments, which is what we call additional data passed to the command. When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. The first word is the command, and the subsequent words are arguments. Observe:

### Solve
**Flag:** `pwn.college{gYI0dmmeqojxCLONFDuPA-AnJAD.QX4YjM1wCMxYzNyEzW}`

I typed hello hackers

```bash
hello hackers
pwn.college{gYI0dmmeqojxCLONFDuPA-AnJAD.QX4YjM1wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## Command History
You're going to type a lot of commands, and typing everything from scratch can be annoying. Luckily, the shell saves a history of every command you invoke.

### Solve
**Flag:** `pwn.college{UOEt14J18KLbIkeA_3RKFj4QpIo.0lNzEzNxwCMxYzNyEzW}`

I hit the up arrow.

```bash
pwn.college{UOEt14J18KLbIkeA_3RKFj4QpIo.0lNzEzNxwCMxYzNyEzW}
```

### New Learnings
None

### References 
None

# 2. Pondering Paths

## The Root
Alright, so the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag. All you need to do for this level is to invoke this program!

### Solve
**Flag:** `pwn.college{ghWQHQKQXxXMl0EiwvgqlRdvF6v.QX4cTO0wCMxYzNyEzW}`

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
/pwd
pwn.college{ghWQHQKQXxXMl0EiwvgqlRdvF6v.QX4cTO0wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## Program and absolute paths
ALet's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

### Solve
**Flag:** `pwn.college{gaofGDfX_H3uaNcQM5Ud0lk_Dt1.QX1QTN0wCMxYzNyEzW}`

Honestly this confused me. I did cd, pwd to check my current location. And then did a lot of stuff found a file named flag which denied me permissions to open the file. But then i did /challenge/run and it worked.

```bash
/challenge/run
pwn.college{gaofGDfX_H3uaNcQM5Ud0lk_Dt1.QX1QTN0wCMxYzNyEzW}
```

### New Learnings
Dont think too much

### References 
None

## Position thy self
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

### Solve
**Flag:** `pwn.college{YjwFI6AfM0dLepvz7qHBCWsG9Y_.QX2QTN0wCMxYzNyEzW}`

At first i did /challenge/run. It said incorrect and that i need to be in in /var/log directory so i went to that directory and ran the program

```bash
hacker@paths~position-thy-self:/home$ /challenge/run
Incorrect...
You are not currently in the /var/log directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:/home$ cd /var/log
hacker@paths~position-thy-self:/var/log$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{YjwFI6AfM0dLepvz7qHBCWsG9Y_.QX2QTN0wCMxYzNyEzW}
hacker@paths~position-thy-self:/var/log$ 
```

### New Learnings
None

### References 
None

## Position elsewhere
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

### Solve
**Flag:** `pwn.college{0pamLLG6Bo_3vV-QgL0hXXkeZpJ.QX3QTN0wCMxYzNyEzW}`

I did the same thing I did in the last challenge.

```bash
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/zoneinfo/posix/Asia directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/share/zoneinfo/posix/Asia
hacker@paths~position-elsewhere:/usr/share/zoneinfo/posix/Asia$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0pamLLG6Bo_3vV-QgL0hXXkeZpJ.QX3QTN0wCMxYzNyEzW}
hacker@paths~position-elsewhere:/usr/share/zoneinfo/posix/Asia$ 
```

### New Learnings
None

### References 
None

## Position yet elsewhere
This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
**Flag:** `ppwn.college{4CO5bEIRL71-mCTVv9zxF7GODaN.QX4QTN0wCMxYzNyEzW}`

Same thing as last time.

```bash
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /tmp
hacker@paths~position-yet-elsewhere:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4CO5bEIRL71-mCTVv9zxF7GODaN.QX4QTN0wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## Implicit relative paths, from /
Let's try it here! You'll need to run /challenge/run using a relative path while having a current working directory of /. For this level, I'll give you a hint. Your relative path starts with the letter c 😊

### Solve
**Flag:** `pwn.college{IKk3l6sZN9NLyyweN3RjwdAO5cr.QX5QTN0wCMxYzNyEzW}`

Well i tried some stuff, then I was was told to access relative path not an absolute path. And when i did so i got the flag.

```bash
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{IKk3l6sZN9NLyyweN3RjwdAO5cr.QX5QTN0wCMxYzNyEzW}

```

### New Learnings
None

### References 
None

## explicit relatives path, from /
Of course, if your current working directory is /, the above relative paths are equivalent to the above absolute paths.

This challenge will get you using . in your relative paths. Get ready!

### Solve
**Flag:** `pwn.college{M_tFB4cVDMWQVwJB-1ibu17G7a9.QXwUTN0wCMxYzNyEzW}`

Yeah same thing basically. But i learned the other ways of calling relative paths.

```bash
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ challenge
bash: challenge: command not found
hacker@paths~explicit-relative-paths-from-:/$ challenge/
bash: challenge/: Is a directory
hacker@paths~explicit-relative-paths-from-:/$ challenge/run
Incorrect...
This challenge must be called with a relative path that explicitly starts with a `.`!
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{M_tFB4cVDMWQVwJB-1ibu17G7a9.QXwUTN0wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## implicit relative path
We'll explore the mechanisms behind this concept later, but in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels. Give it a try now!

### Solve
**Flag:** `pwn.college{gQl_iiG-2jg2Xy9u4AI53pGo7P4.QXxUTN0wCMxYzNyEzW}`

I did ./run to execute the program.

```bash
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{gQl_iiG-2jg2Xy9u4AI53pGo7P4.QXxUTN0wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## home sweet home
Now it's your turn to play! In this challenge, /challenge/run will write a copy of the flag to any file you specify as an argument on the commandline, with these constraints:

Your argument must be an absolute path.
The path must be inside your home directory.
Before expansion, your argument must be three characters or less.
Again, you must specify your path as an argument to /challenge/run as so: 

### Solve
**Flag:** `pwn.college{UqkG_GAnPijTXWitMAPg9la0K7t.QXzMDO0wCMxYzNyEzW}`

I tried many things. I understood that the your path name must be only 3 characters in here for copying the file. So what i did inititally was try doing /challenge/run ~ and it didnt work. So when i kept looking at the question they created a file using ~/asdf. So when i tried doing it it worked.

```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/asdf
The argument you provided must not have been longer than 3 characters (it's 
currently 6 characters long)!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{UqkG_GAnPijTXWitMAPg9la0K7t.QXzMDO0wCMxYzNyEzW}
```

### New Learnings
I learnt how to copy of the program to the file.

### References 
None
