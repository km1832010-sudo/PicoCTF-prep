#OTW Bandit Writeup: 18

Objective: log into something other than .bashrc

 The website mentions we are being forcefully kicked out of .bashrc shell, after some searching, I found i could force myself into a different shell using the -t option for ssh. This second part would've taken a while if not for google ai summary, but another shell that is almost always found it /bin/sh, it interprets symbolic links(dw about this till leviathan) and so it is is usually present:

``` ssh bandit18@bandit.labs.overthewire.org -p 2220 -t /bin/bash```

Then i just cat the readme file to get the flag

Flag: cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8