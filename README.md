DESCRIPTION

Let there be n agents and n tasks. Any agent can be assigned to perform any task, 
incurring some cost that may vary depending on the agent-task assignment. 
It is required to perform all tasks by assigning exactly one agent to each 
task and exactly one task to each agent in such a way that the total cost of the 
assignment is minimized. Example: You work as a manager for a chip manufacturer, 
and you currently have 3 people on the road meeting clients. Your salespeople are in 
Jaipur, Pune and Bangalore, and you want them to fly to three other cities: Delhi, 
Mumbai and Kerala. The table below shows the cost of airline tickets in INR between the cities:

![Test Image 1](images/1.jpg)

The question: where would you send each of your salespeople in order to minimize fair?

Possible assignment: Cost = 11000 INR

![Test Image 1](images/2.jpg)

Other Possible assignment: Cost = 9500 INR and this is the best of the 3! possible assignments.

![Test Image 1](images/3.jpg)

Brute force solution is to consider every possible assignment implies a complexity of Ω(n!).

The Hungarian algorithm, aka Munkres assignment algorithm, utilizes the following theorem for polynomial runtime complexity (worst case O(n3)) and guaranteed optimality: If a number is added to or subtracted from all of the entries of any one row or column of a cost matrix, then an optimal assignment for the resulting cost matrix is also an optimal assignment for the original cost matrix.

We reduce our original weight matrix to contain zeros, by using the above theorem. We try to assign tasks to agents such that each agent is doing only one task and the penalty incurred in each case is zero.