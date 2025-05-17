# EX:5C - Kadane's Algorithm
## DATE:

## AIM:

To write a python program to find the maximum contiguous subarray.


## Algorithm

1. Initialize Variables, max_till_now is set to the first element (to handle all-negative arrays), max_ending is initialized to 0 (tracks sum of the current 
   subarray).
2. Loop through each element, adding it to max_ending.
3. If max_ending becomes negative, reset it to 0 (discard the subarray as it reduces the sum).
4. Update max_till_now if max_ending exceeds the current maximum.
5. After the loop, max_till_now holds the maximum subarray sum.  

## Program:
```
To implement the program to find the maximum contiguous subarray

DEVELOPED BY    : NIRAUNJANA GAYATHRI G R
REGISTER NUMBER : 212222230096
```
```
def maxSubArraySum(a,size):
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        elif (max_till_now < max_ending):
            max_till_now = max_ending
    return max_till_now
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output:

![image](https://github.com/user-attachments/assets/aeb0b653-338d-43f6-9e47-0fad3e9dcd99)


## Result:

Thus the program was executed successfully for finding the maximum contiguous sum of subarray.
