#OTW Bandit Writeup: 8

Objective: Find the only unique line in a large list

To do this we must use the ```uniq``` command with the -u option. That will give us the only unique line in the list however as a precondition we need to sort the list. The obvious solutions is to use ```sort```, but how can we input the sorted list into uniq? The solution is piping. The | symbol will act as a pipe or "then" symbol. it takes the output from the left side of the expression and inputs it into the right side or it simply just does both commands in succession if the first one doesn't have any output(like cd).

The final solution is:  sort data.txt | uniq -u

Flag:4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

