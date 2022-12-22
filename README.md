# Rideshare Application

My main starts with some input checks. First, if there are 3 inputs. The program, team a fans and team b fans. Then, it checks if the fans are < 0, if there are even numbers of fans from each team and if the sum of fans can be divided by 4. If any of these fail, the program returns with 1, 2 or 3(for each error). Then threads are created, and we use the functions.

I created 2 functions to check for each teams’ fans. At the start of the program, functions are called, and they add each fan. Then they check the possible matchings 2-2 and 4-0 for their team. Each fan will wait at the end of the function until there are 4 fans. I’ve achieved these using semaphores and a barrier. 
There are 2 mutexes, one to lock functions and the other to lock captains so that there are no race conditions. At the end, threads join, and the program is terminated.
