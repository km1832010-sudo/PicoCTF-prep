#OTW Bandit Writeup: 6

Objective: find a file on the whole server with these properties
owned by user bandit7
owned by group bandit6
33 bytes in size

The challenge here is that because the server is large there will be many different files unless we use all given attributes. First of all we go to the root by doing ```cd ..``` twice. Then to include all given attributes we run: ``` find . -user "bandit7" -group "bandit6" -size 33c ``` which are all publicly available options. There is only one file among the given list without "permission denied" next to it so we cat it to get the flag. (there is a way to filter but the current you is too lazy to find it)

Flag:morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj