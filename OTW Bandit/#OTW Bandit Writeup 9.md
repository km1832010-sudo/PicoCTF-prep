#OTW Bandit Writeup: 9

Objective: Use grep to find a string in a binary file

usually grep wont work on a binary file. Using the -a option we can force it to. For the string we can put any reasonable amount of ='s.: ```grep -a "=====" data.txt```
 
Flag:FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey