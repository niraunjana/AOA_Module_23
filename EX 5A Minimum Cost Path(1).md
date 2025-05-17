# EX:5A - Minimum Cost Path
## DATE:

## AIM:

To write a Python program using A Naive recursive implementation of Minimum Cost Path Problem.

## Algorithm

1. Accept dimensions R (rows) and C (columns) of a 2D cost matrix from the user.
2. Define a function minCost that recursively computes the minimum cost to reach cell (m, n) from (0, 0) by only moving right, down, or diagonally down-right.
3. If the indices are negative, return a very large number (sys.maxsize) to prevent invalid moves. If (m, n) is the origin (0, 0), return the cost at that cell.
4. At each step, choose the minimum cost path by considering three possible directions (from top, left, or diagonal).
5. Call minCost(cost, R-1, C-1) to calculate the minimum cost path to the bottom-right corner and print the result.

## Program:
```
A program to implement to find the Minimum Cost Path Problem using a  Naive recursive Approach

DEVELOPED BY     : NIRAUNJANA GAYATHRI G R 
REGISTER NUMBER  : 212222230096
```
```
R = int(input())
C = int(input())
import sys
def minCost(cost, m, n):
    if (n < 0 or m < 0):
        return sys.maxsize
    elif (m == 0 and n == 0):
        return cost[m][n]
    else:
        return cost[m][n] + min( minCost(cost, m-1, n-1),
                                minCost(cost, m-1, n),
                                minCost(cost, m, n-1) )
def min(x, y, z):
    if (x < y):
        return x if (x < z) else z
    else:
        return y if (y < z) else z
cost= [ [1, 2, 3],
        [4, 8, 2],
        [1, 5, 3] ]
print(minCost(cost, R-1, C-1))
```

## Output:

![image](https://github.com/user-attachments/assets/f22165a4-d4a1-441a-a597-659cf3f94431)

## Result:

Thus the above program was executed successfully for finding the minimum cost.
