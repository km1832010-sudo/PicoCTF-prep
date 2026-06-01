#OTW Bandit Writeup: 2

Objective: cat a file with spaces in its name

The file has spaces so simply putting ./ the name wont work as it will be interpreted as multiple files. the --  at the beginning also means  making it a string with quotations wont work as the kernel will read it as an option. What we have to do it combine these approaches:
```cat ./"--spaces in this filename--" ```

Flag:MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx