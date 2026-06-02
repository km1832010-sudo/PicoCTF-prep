#OTW Bandit Writeup: 5

Objective: find a file with these qualities:
human-readable
1033 bytes in size
not executable

So we cant just brute force like last time as there are way too many files. There are also various directories. The easiest method to find the file is using the find command. We start by using the ```-size``` option as it narrows the results down the most.

```find -size 1033c```(c to specify that the number refers to bytes) we get ./maybehere07/.file2 as a result, so we cat it



Flag:HWasnPhtq9AVKe0dmk45nxy20cvUa6EG