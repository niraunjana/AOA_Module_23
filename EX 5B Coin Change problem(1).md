# EX:5B - Coin Change Problem
## DATE:

## AIM:

To compute the fewest number of coins that we need to make up the amount given.

## Algorithm

1. Create a dp array of size amount + 1, filled with inf (representing an unreachable state), and set dp[0] = 0 (0 coins needed to make amount 0).
2. Loop through each coin in the coins list to determine how each coin can contribute to building up the total amount.
3. For each coin, iterate from its value up to the target amount, and update dp[i] using the formula:
   - dp[i] = min(dp[i], dp[i - coin] + 1)
   - This represents taking the minimum coins needed to form i.
4. After processing all coins, dp[amount] contains the minimum number of coins required to form the target amount.
5. If dp[amount] is still inf, return -1 (not possible to form the amount), else return dp[amount].

## Program:
```
Create a python function to compute the fewest number of coins that we need to make up the amount given

DEVELOPED BY    : NIRAUNJANA GAYATHRI G R
REGISTER NUMBER : 212222230096
```
```
class Solution(object):
   def coinChange(self, coins, amount):
       dp = [float('inf')] * (amount + 1)
       dp[0]=0
       for coin in coins:
           for i in range(coin, amount + 1):
               dp[i] = min(dp[i], dp[i - coin] + 1)
       return dp[amount] if dp[amount]!=float('inf') else -1
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))

print(ob1.coinChange(s,amt))
```


## Output:

![image](https://github.com/user-attachments/assets/993c4b0d-cbb3-473d-8b9e-b1e608a9b2db)

## Result:

Thus the program was executed successfully for finding the minimum number of coins required to make amount.
