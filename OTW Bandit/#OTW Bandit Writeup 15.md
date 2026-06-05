#OTW Bandit Writeup: 15

Objective: Connect to localhost port 30001 with an ssl encryption

An ssl encryption is meant to protect a network's data and make it harder to view from an outside perspective, as it would need decryption. The port requires us to connect with an ssl connection. The website recommends using openssl and s_client as some of the commands. Since these are related to ssl I checked them out.

Openssl has its own commands, looking at the command list one of them is s_client, so by running ```openssl s_client``` it tells us to add the -help option. At the very bottom of the list of commands/options the syntax is shown: ```openssl s_client localhost:30001 ```

Then by sending the current level's password we get the flag.
 
Flag:kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx