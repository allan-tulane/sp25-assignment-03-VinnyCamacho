# CMPS 2200 Assignment 3
## Answers

**Name:**
Vincent Camacho


Place all written answers from `assignment-03.md` here for easier grading.


1. Greedy Algo (assuming that the coins represent powers of 2 in dollars and not in cents, so 1 dollar coins, 2 dollar coins, not 1 cent, 2 cents, 4 cents, etc.)
While N > 0:
  choose largest_coin less than total dollars (N)
  subtract that coins value from the total (N -= largest_coin)
  
