---
title: We must use "time" creatively. - Martin Luther King, Jr.
date: 2016-10-04 15:58:01
excerpt: false
tags:
- linux
- shell
- bash
- zsh
- command
---

The default `time` command in most Linux distributions is not a REAL command, it comes as built-in functionality of shells like "bash".

But, when you type `man time`, you will get a manual for a time utility which may not be installed.

For example, in Arch Linux, run `sudo pacman -S time` to install the GNU version of the "time" utility, then you can run the following commands (It's important to run it with the full path, otherwise 
you will be running the built-in "time" command):

```
/usr/bin/time uname
/usr/bin/time -v uname
```

You will notice that the output is slightly different to the output of the built-in "time" command.

Running the following command will produce a similar output to the built-in "time" function:

```
/usr/bin/time -f "%C  %Us user %Ss system %P cpu %e total" uname
```

Have fun :-)
