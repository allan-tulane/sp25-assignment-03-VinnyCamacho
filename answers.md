# CMPS 2200 Assignment 3
## Answers

**Name:**
Vincent Camacho


Place all written answers from `assignment-03.md` here for easier grading.


1a. Greedy Algo (assuming that the coins represent powers of 2 in dollars and not in cents, so 1 dollar coins, 2 dollar coins, not 1 cent, 2 cents, 4 cents, etc.)
While N > 0:
  choose largest_coin less than total dollars (N)
  subtract that coins value from the total (N -= largest_coin)
  
1b. The greedy choice is choosing the largest possible coin less than N, or the largest power of 2 less than N, because this allows the fewest coins to be used. This is because all coins are powers of 2, so using a smaller value would require more coins. This creates a substucture of N - 2^k where k is a positive integer, and this subproblem can be solved in the same way as the previous, making this an optimal substructure.

1c. The worst case is that input size is divided in half each iteration, making the work O(logn), and since the work is sequential as each step is dependent on the last, the span is also O(logn)

2a. The greedy algorithm of choosing the largest value less than the input size will not always minimize the number of coins as it did in the previous question. For example, if the denominations are: {1, 3, 4}, and you have to make change for N = 6. The greedy algorithm would chose 4, now N = 2 so 1, then N = 1 so choose 1, for a total of 4,1,1. The optimal solution is 3 and 3, only 2 coins, but does not follow the rules of the greedy algorithm. 

2b. Let C(N) = minimum coins to make change N. Then:
C(N) = min(C(N-di) + 1) where di is a coin denomination used by a given bank.
If the way to make change with the fewest coins uses a denomination di, then the subproblem is now N - di, which should have an optimal solution given the denominations available
