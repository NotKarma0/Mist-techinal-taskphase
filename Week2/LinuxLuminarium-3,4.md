# 3. Comprehending Commands

## cat: not the pet, but the command!
Finally, if you give no arguments at all, cat will read from the terminal input and output it. We'll explore that in later challenges...

In this challenge, I will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!

### Solve
**Flag:** 'pwn.college{8y1_pe8WeA1yPp_g6BJLCpPWGRk.QXxcTN0wCMxYzNyEzW}'
I typed cat flag.

```bash
hacker@commands~cat-not-the-pet-but-the-command:/$ cat flag
pwn.college{8y1_pe8WeA1yPp_g6BJLCpPWGRk.QXxcTN0wCMxYzNyEzW}
```

### New Learnings
None

### References 
None

## cat absolute paths
In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.

FUN FACT: /flag is where the flag always lives in pwn.college, but unlike in this challenge, you typically can't access that file directly.

### Solve
**Flag:** 'pwn.college{Uyi2cJE6MAXA1-9fJZile96jbqm.QX5ETO0wCMxYzNyEzW}'

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{Uyi2cJE6MAXA1-9fJZile96jbqm.QX5ETO0wCMxYzNyEzW}
```
### New Learning
None

### References
None

## more catting practice
You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you. You must retrieve the flag by absolute path, wherever it is.

### Solve
**Flag:** 'pwn.college{8UKcC8BdjPSI68kJaeb99bGZ_cp.QXwITO0wCMxYzNyEzW}'

```bash
hacker@commands~more-catting-practice:~$ cat /lib/x86_64-linux-gnu/perl-base/flag
pwn.college{8UKcC8BdjPSI68kJaeb99bGZ_cp.QXwITO0wCMxYzNyEzW}
```

### New Learning
None

### References
None

## grepping for a needle in a haystack
Invoked like this, grep will search the file for lines of text containing SEARCH_STRING and print them to the console.

In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!

HINT: The flag always starts with the text pwn.college.

### Solve
**Flag:** 'pwn.college{0XNOF4iCnyHZ_k7plA7pX8slhv_.QX3EDO0wCMxYzNyEzW}'

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{0XNOF4iCnyHZ_k7plA7pX8slhv_.QX3EDO0wCMxYzNyEzW}
```

### New Learning
grep finds a text to search in a big paragraph or stuff.

### References
None

## comparing files
This tells us that after line 1 in the first file, the second file has an additional line (1a2 means "after line 1 of file1, add line 2 of file2").

Now for your challenge! There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags
/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag
Use diff to find what's different between these files and get your flag!

### Solve
**Flag:** 'pwn.college{cwqpVghH0EhVON1HRKLFZjZxDpE.01MwMDOxwCMxYzNyEzW}'

```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
97a98
> pwn.college{cwqpVghH0EhVON1HRKLFZjZxDpE.01MwMDOxwCMxYzNyEzW}
```

### New Learning
diff gets the difference between two files.

### References
None

## listing files
In this challenge, we've named /challenge/run with some random name! List the files in /challenge to find it.

### Solve
**Flag:** 'pwn.college{wFj9KzXMy12t6PBuOem_aYln0O-.QX4IDO0wCMxYzNyEzW}'

```bash
hacker@commands~listing-files:/challenge$ ls /challenge
15590-renamed-run-18885  DESCRIPTION.md
hacker@commands~listing-files:/challenge$ cat 15590-renamed-run-18885
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:/challenge$ cat /flag
cat: /flag: Permission denied
hacker@commands~listing-files:/challenge$ ./15590-renamed-run-18885
Yahaha, you found me! Here is your flag:
pwn.college{wFj9KzXMy12t6PBuOem_aYln0O-.QX4IDO0wCMxYzNyEzW}
```

### New Learning
None

### References
None

## touching files
It's that simple! In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag!

### Solve
**Flag:** 'pwn.college{YUeLfTwS2CNCGIva-txLLloCzI2.QXwMDO0wCMxYzNyEzW}'

```bash
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{YUeLfTwS2CNCGIva-txLLloCzI2.QXwMDO0wCMxYzNyEzW}
```

## removing files
Let's practice. This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag!

### Solve
**Flag:** 'pwn.college{8VNExJLIJzhIIS95hssh2RyPJGj.QX2kDM1wCMxYzNyEzW}'

```bash
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{8VNExJLIJzhIIS95hssh2RyPJGj.QX2kDM1wCMxYzNyEzW}
```

### New Learning
None

### References
None

## moving files
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

### Solve
**Flag:** 'pwn.college{sPMnefM4T1LUfM7-JxFVgptBgcA.0VOxEzNxwCMxYzNyEzW}'

```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{sPMnefM4T1LUfM7-JxFVgptBgcA.0VOxEzNxwCMxYzNyEzW}
```

### New Learning
None

### References
None

## copying files
But what if you want to keep the original file? You can do so with the cp command. The usage is the same as with mv, but it will keep the source file.

This challenge wants you to copy the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

### Solve
**Flag:** 'pwn.college{IohBrt_d_uayZdWcea6L1DUnsxI.0lNxQTMywCMxYzNyEzW}'

```bash
hacker@commands~copying-files:~$ cp /flag /tmp/hack-the-planet
Correct! Performing 'cp /flag /tmp/hack-the-planet'.
hacker@commands~copying-files:~$ /challenge/check
Congrats! You successfully copied the flag to /tmp/hack-the-planet! Here it is:
pwn.college{IohBrt_d_uayZdWcea6L1DUnsxI.0lNxQTMywCMxYzNyEzW}
```

### New Learning
None

### References
None

## hidden files
Now, it's your turn! Go find the flag, hidden as a dot-prepended file in /.

### Solve
**Flag:** 'pwn.college{EzWBU6lwNVNkLc5MX7h6b0koUBA.QXwUDO0wCMxYzNyEzW}'

```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-22261324728176  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat flag-22261324728176
cat: flag-22261324728176: No such file or directory
hacker@commands~hidden-files:/$ ls flag-22261324728176
ls: cannot access 'flag-22261324728176': No such file or directory
hacker@commands~hidden-files:/$ cat .flag-22261324728176
pwn.college{EzWBU6lwNVNkLc5MX7h6b0koUBA.QXwUDO0wCMxYzNyEzW}
```

### New Learning
None

### References
None

## An Epic Filesystem Quest
In this challenge, I have hidden the flag! Here, you will use ls and cat to follow my breadcrumbs and find it! Here's how it'll work:

Your first clue is in /. Head on over there.
Look around with ls. There'll be a file named HINT or CLUE or something along those lines!
cat that file to read the clue!
Depending on what the clue says, head on over to the next directory (or don't!).
Follow the clues to the flag!

### Solve
**Flag:** 'pwn.college{I87LXvbxdRmmrRSbVdrlUJlNg36.QX5IDO0wCMxYzNyEzW}'

```bash
too many commands
```

### New Learning
None

### References
None

## making directories
Now, go forth and create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag!

### Solve
**Flag:** 'pwn.college{46SfYExHwUKNsA9rKZUPxZU3djP.QXxMDO0wCMxYzNyEzW}'

```bash
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:~$ touch /tmp/pwn/college
hacker@commands~making-directories:~$ /challenge/run
Success! Here is your flag:
pwn.college{46SfYExHwUKNsA9rKZUPxZU3djP.QXxMDO0wCMxYzNyEzW}
```

### New Learning
None

### References
None

## finding files
Now it's your turn. I've hidden the flag in a random directory on the filesystem. It's still called flag. Go find it!

Several notes. First, there are other files named flag on the filesystem. Don't panic if the first one you try doesn't have the actual flag in it. Second, there're plenty of places in the filesystem that are not accessible to a normal user. These will cause find to generate errors, but you can ignore those; we won't hide the flag there! Finally, find can take a while; be patient!

### Solve
**Flag:** 'pwn.college{MrCemwEEPvcrYesDvLgCava-OXV.QXyMDO0wCMxYzNyEzW}'

```bash
find / -name flag
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/lib/debug/.build-id/6c/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag
/nix/store/h88mxp2mbgyj06vypwmqpy05idhwimnp-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag
/nix/store/5qz6hgb1qzpvjrsw20wyiylx5zw8b9bk-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag
cat /usr/lib/debug/.build-id/6c/flag
pwn.college{MrCemwEEPvcrYesDvLgCava-OXV.QXyMDO0wCMxYzNyEzW}
```

### New Learning
How to use find command.

### References
None

## linking files 
Okay, now you try it! In this level the flag is, as always, in /flag, but /challenge/catflag will instead read out /home/hacker/not-the-flag. Use the symlink, and fool it into giving you the flag!

### Solve
**Flag:** 'pwn.college{UgmAdVQ7b-6iHqpFhaHdO0B5aom.QX5ETN1wCMxYzNyEzW}'

```bash
hacker@commands~linking-files:~$ cat /flag
cat: /flag: Permission denied
hacker@commands~linking-files:~$ cat /challenge/catflag
#!/opt/pwn.college/bash
fold -s <<< "About to read out the /home/hacker/not-the-flag file!"
cat /home/hacker/not-the-flag
hacker@commands~linking-files:~$ cat /home/hacker/not-the-flag
cat: /home/hacker/not-the-flag: No such file or directory
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{UgmAdVQ7b-6iHqpFhaHdO0B5aom.QX5ETN1wCMxYzNyEzW}
```

### New Learning 
Hose to link files.

### References
None

# 4. Digesting Documentation
## Learning from documentation
The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag. Let's pretend that this is its documentation:

Welcome to the documentation for /challenge/challenge! To properly run this program, you will need to pass it the argument of --giveflag. Good luck!

Given that knowledge, go get the flag!

### Solve
**Flag:** 'pwn.college{g8rp7Le6FwEj5MYUfoqpm3iNfqb.QX0ITO0wCMxYzNyEzW}'

```bash
hacker@man~learning-from-documentation:~$ ls -l
total 8
-rw-r--r-- 1 root   hacker 60 Nov  4 08:48 a
lrwxrwxrwx 1 hacker hacker  5 Nov 13 10:44 not-the-flag -> /flag
hacker@man~learning-from-documentation:~$ ls -a
.  ..  .bash_history  .cache  .config  .local  a  not-the-flag
hacker@man~learning-from-documentation:~$ cat /flag
cat: /flag: Permission denied
hacker@man~learning-from-documentation:~$ /not-the-flag
bash: /not-the-flag: No such file or directory
hacker@man~learning-from-documentation:~$ ln -s /flag /challenge/challenge
ln: failed to create symbolic link '/challenge/challenge': File exists
hacker@man~learning-from-documentation:~$ /challenge/challenge
Incorrect usage! You must pass an argument to me (read the challenge 
description for details).
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{g8rp7Le6FwEj5MYUfoqpm3iNfqb.QX0ITO0wCMxYzNyEzW}
```

### New Learning 
How to pass by an argument.

### References
None

## Learning complex usage
Here is this level's documentation for /challenge/challenge:

Welcome to the documentation for /challenge/challenge! This program allows you to print arbitrary files to the terminal, when given the --printfile argument. The argument to the --printfile argument is the path of the flag to read. For example, /challenge/challenge --printfile /challenge/DESCRIPTION.md will print out the description of the level!

Given that documentation, go get the flag!

### Solve
**Flag:** 'pwn.college{szm3YtXRdyx2aPYPTW0LzLhyUYO.QX1ITO0wCMxYzNyEzW}'

```bash
hacker@man~learning-complex-usage:~$ cat /not-the-flag
cat: /not-the-flag: No such file or directory
hacker@man~learning-complex-usage:~$ cat /flag
cat: /flag: Permission denied
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{szm3YtXRdyx2aPYPTW0LzLhyUYO.QX1ITO0wCMxYzNyEzW}
```

### New Learning 
Learned how to give pass by argument to pass by argument.

### References
None

## Reading manuals
Manpages are stored in a centralized database. If you're curious, this database lives in the /usr/share/man directory, but you never need to interact with it directly: you just query it using the man command. The arguments to the man command aren't file paths, but just the names of the entries themselves (e.g., you run man yes to look up the yes manpage, rather than man /usr/bin/yes, which would be the actual path to the yes program but would result in man displaying garbage).

The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for challenge!


### Solve
**Flag:** 'pwn.college{MHjzQndPsF1YWAS_AW1IGtV6ypM.QX0EDO0wCMxYzNyEzW}'

```bash
man challenge
/challenge/challenge --jzndst 116
Correct usage! Your flag: pwn.college{MHjzQndPsF1YWAS_AW1IGtV6ypM.QX0EDO0wCMxYzNyEzW}
```

### New Learning 
What is a man file.

### References
None

## Searching manuals
You can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, you can hit n to go to the next result and N to go to the previous result. Instead of /, you can use ? to search backwards!

Find the option that will give you the flag by reading the challenge man page.

### Solve
**Flag:** 'pwn.college{MglWuH3HZmNuGQfknt4KA-mvU6H.QX1EDO0wCMxYzNyEzW}'

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ccvibx
Initializing...
Incorrect usage! Please read the challenge man page!
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ccivbx
Initializing...
Correct usage! Your flag: pwn.college{MglWuH3HZmNuGQfknt4KA-mvU6H.QX1EDO0wCMxYzNyEzW}
```

### New Learning 
How to search in a man file using /.

### References
None

## Searching for manuals
HINT 1: man man teaches you advanced usage of the man command itself, and you must use this knowledge to figure out how to search for the hidden manpage that will tell you how to use /challenge/challenge

HINT 2: though the manpage is randomly named, you still actually use /challenge/challenge to get the flag!

### Solve
**Flag:** 'pwn.college{ofOlZNA1YGo3scM7dWQmE6dmYdY.QX2EDO0wCMxYzNyEzW}'

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man /challenge/challenge
hacker@man~searching-for-manuals:~$ man --oflosc 137
man: unrecognized option '--oflosc'
Try 'man --help' or 'man --usage' for more information.
hacker@man~searching-for-manuals:~$ /challenge/challenge --oflosc 137
Correct usage! Your flag: pwn.college{ofOlZNA1YGo3scM7dWQmE6dmYdY.QX2EDO0wCMxYzNyEzW}
```

### New Learning 
Idk, still in doubt.

### References
Chatgpt.

## Helpful programs
Some programs don't have a man page, but might tell you how to run them if invoked with a special argument. Usually, this argument is --help, but it can often be -h or, in rare cases, -?, help, or other esoteric values like /? (though that latter is more frequently encountered on Windows).

In this level, you will practice reading a program's documentation with --help. Try it out!

### Solve
**Flag:** 'pwn.college{kJq3mqbsVtRqKabqpNdLDEthmOk.QX3IDO0wCMxYzNyEzW}'

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -h
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 330
hacker@man~helpful-programs:~$ /challenge/challenge -g GIVE_THE_FLAG 330
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]
a challenge to make you ask for help: error: argument -g/--give-the-flag: invalid int value: 'GIVE_THE_FLAG'
hacker@man~helpful-programs:~$ /challenge/challenge -g 330
Correct usage! Your flag: pwn.college{kJq3mqbsVtRqKabqpNdLDEthmOk.QX3IDO0wCMxYzNyEzW}
```

### New Learning 
Help command --help, help, -h, -?, help, /?

### References
None

## Help for builitins
Some good information! In this challenge, we'll practice using help to look up help for builtins. This challenge's challenge command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!

### Solve
**Flag:** 'pwn.college{wrxDkbuKMp7YyJ67r0hssluj47T.QX0ETO0wCMxYzNyEzW}'


```bash
hacker@man~help-for-builtins:~$ help challenge
hacker@man~help-for-builtins:~$ /challenge --secret wrxDkbuK
bash: /challenge: Is a directory
hacker@man~help-for-builtins:~$ ./challenge --secret wrxDkbuK
bash: ./challenge: No such file or directory
hacker@man~help-for-builtins:~$ challenge --secret wrxDkbuK
Correct! Here is your flag!
pwn.college{wrxDkbuKMp7YyJ67r0hssluj47T.QX0ETO0wCMxYzNyEzW}
```

### New learning
None

### References
None
