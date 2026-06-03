#OTW Bandit Writeup: 13

Objective: Use an RSA key to login to bandit14

When we log in to bandit 13 we get and rsa and a hint file. Ignoring the hint file cat the rsa key. This is all we need to log in to bandit 14. Now we just have to echo it into a file like this: ```echo "pasteFullKeyHere">filename```

We can then use the -i identifier option to add the key to out ssh, but it will be declined as the permissions are too open. We have to use chmod, a command that sets a files permissions and its very expansive so i suggest reading the man. The standard rsa key permission is 600 so we do ```chmod 600 filename```.

The final ssh with the name i used looks like this: ```ssh bandit14@bandit.labs.overthewire.org -p 2220 -i bandit14rsakey```

We can then cat /etc/bandit_pass/bandit14 as the website says to get the flag.
 
Flag:MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS