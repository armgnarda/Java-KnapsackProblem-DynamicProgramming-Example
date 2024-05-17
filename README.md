# Java-KnapsackProblem-DynamicProgramming-Example
The knapsack problem involves selecting items with given weights and values to maximize the total value without exceeding a specified weight limit.

The knapsack problem is an optimization problem where a thief needs to make choices among various items, each with a specific weight and value, while respecting the capacity of a given knapsack. Each item has both a value (such as an amount of money) and a weight. The thief's objective is to maximize the total value of the items they select for the knapsack without exceeding its capacity. This problem can be solved using methods like dynamic programming, which involves solving smaller subproblems and using those solutions to solve larger ones. The knapsack problem finds applications in various fields such as supply chain management, financial portfolio optimization, and data compression.

pseudo code:

    Knapsack(W, wt[], val[], n):
    DP = 2D array with dimensions (n+1) x (W+1)

    for i from 0 to n:
        for w from 0 to W:
            if i == 0 or w == 0:
                DP[i][w] = 0
            else if wt[i-1] <= w:
                DP[i][w] = max(val[i-1] + DP[i-1][w - wt[i-1]], DP[i-1][w])
            else:
                DP[i][w] = DP[i-1][w]

    return DP[n][W]
