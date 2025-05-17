# EX:5D - Minimum Jump to Reach End Array
## DATE:

## AIM:

To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm:

1. Base case checking, if the current index l is already at the destination h, return 0 (no jumps needed).
2. If the current element is 0, we can't jump further, so return infinity.
3. Set a variable min to infinity to keep track of the minimum jumps needed.
4. For each index reachable from l, recursively calculate the jumps to the end and update min if a better path is found.
5. Return the minimum number of jumps required from index l to h.

## Program:
```
To implement the program to finding the minimum number of jumps needed to reach end of the array

DEVELOPED BY    : NIRAUNJANA GAYATHRI G R
REGISTER NUMBER : 212222230096
```
```
def minJumps(arr, l, h):
    if (h == l):
        return 0
    if (arr[l] == 0):
        return float('inf')
    min = float('inf')
    for i in range(l + 1, h + 1):
        if (i < l + arr[l] + 1):
            jumps = minJumps(arr, i, h)
            if (jumps != float('inf') and
                       jumps + 1 < min):
                min = jumps + 1
    return min  
arr = []
n = int(input()) 
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr, 0, n-1))
 
```

## Output:

![image](https://github.com/user-attachments/assets/b931e611-b506-4fa2-8c2e-b30726d6e4c2)


## Result:

Thus the program was executed successfully for finding the minimum number of jumps to reach end.
