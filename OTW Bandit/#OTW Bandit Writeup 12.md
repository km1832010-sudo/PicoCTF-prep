#OTW Bandit Writeup: 12

Objective: Revert a file to ASCII after many compressions

The main key to this objective is the ```file``` command. It gives us the status of the file. It starts by saying its ASCII but if we cat it we can see its actually a hexdump. 

Another challenge is figuring out how to modify the file, even though you could take the initial hexdump and run it through various different recipes on [cyberchef](https://gchq.github.io/CyberChef), its a lot easier on a Linux kernel. We have little permissions in the home directory, but as the website states we have a lot more freedom in the /tmp directory. Using ```mktmp /tmp/XXXXX``` We get a randomly named directory in /tmp. (```mkdir /tmp/"whatever name"``` can also be used).

After we have made the new directory we can move there with the ```cp``` command as it can copy a files contents: ``` cp ~/data.txt ./data.txt```

Now back to the hexdump. To undo it we must use ```xxd -r``` on the file, but this will output it to the kernel. There are many ways to get it in a file such as using the > or >> symbols on a new file, or using echo, but personally i just did ```xxd -r ~/data.txt>./data.txt``` after using ```rm``` on data.txt to remove it. 

Next the file tells us its a gzip file, we must give it a .gz suffix for gzip commands to be able to affect it. I used cp again and then after it was moved to a file with the correct file i used ```gzip -d``` to decompress it. This left me with a stripped file called "data" because gzip removes the suffix after decompressing.

Next is bzip2 which follows the same process as gzip, but with a .bz2 suffix.

The last type of file was tar. We need to use -x to extract with tar and -f to make it work on files. This looks like ```tar -x -f data``` and leaves you with a .bin file.

Repeat these processes depending in which output file gives you and eventually you'll reach an ASCII that contains the flag. 


Flag:FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn