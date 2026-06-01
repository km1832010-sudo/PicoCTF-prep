#OTW Bandit Writeup: 1

Objective: Login and cat a file named - . 

If a normal cat is used on it, it wont work because the - is also used for flags(options) making it a special symbol. To prevent the kernel as reading it as the start of a flag I will path to the file first: ```cat ./- ``` 


Flag:263JGJPfgU6LtdEvgfWU1XP5yac29mFx