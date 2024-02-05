# Return Two Numbers from a List

## Directions
Given a list of numbers and a number k, return whether any two numbers from the list add up to k. <br>
<br>
For example, given [10, 15, 3, 7] and k of 17, return true since 10 + 7 is 17.

## Solution
1. Create a function
```
def findpair(list1, k):
```
2. Create two for loops within the function to go through every number possible combination:
```
def findpair(list1, k):
  for i in range(0, len(list1)):
    for j in range(0, len(list1)):
```
3. Add an if statement that checks through the addition of the numbers in the list to see if the addition of the number is True or False
## Final Solution
```
def findpair(list1, k):
    for i in range(0, len(list1)):
        for j in range(0, len(list1)):
            if k == list1[i] + list1[j]:
                return True
        return False
```
## Testing the Code
```
def findpair(list1, k):
    for i in range(0, len(list1)):
        for j in range(0, len(list1)):
            if k == list1[i] + list1[j]:
                return True
        return False

# Example List - nums
nums = [10, 5, 6, 7, 3]
# Example number k to see if any numbers in the list add to k
k = 17
print(findpair(nums, k))
```
