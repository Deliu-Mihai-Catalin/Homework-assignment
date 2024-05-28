isPossible Function:
-This function checks if it's possible to allocate books in a way that no employee gets more than a given maximum load.
-It iterates through the books, accumulating their sizes until the maximum load is reached for an employee.

findMinMaxLoad Function:
-This function finds the minimum possible maximum load using binary search.
-It gives a random number between 0 and the sum of all book sizes.
-At each iteration of the binary search, it checks if the current mid-point value is possible using the "isPossible" function.

Random Data Generation:
-The program generates random page numbers for each book within a specified range using the "rand()" function and seeds the random number generator with the current time to ensure different sequences of random numbers each time the program runs.
  
