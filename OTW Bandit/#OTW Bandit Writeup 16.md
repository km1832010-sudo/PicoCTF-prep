#OTW Bandit Writeup: 16

Objective: identify open ports in a range and the type of connection needed

overall to find and identify ports, nmap is  the best option. By reading the syntax at the beginning we find the initial command to be ``` nmap -p 31000-32000 localhost```. This however isn't enough as it doesn't show the type of connect needed, so we need to add the -sV option(this will take considerably longer, like 2-3 mins).

Now we just need to connect to each of the ports and send the password. Last time I used telnet to do this, but I'm gonna use the overall better tool nc. For the ssl ports though i used ncat, which is the same tool, but im pretty sure they have different options. Ncat has the --ssl option. Going port by port i found port 31790 to be the correct one and got an rsa key from there. If you need help using the rsa go back to bandit 13.

Flag: RSA:EReVavePLFHtFlFsjn3hyzMlvSuSAcRD
