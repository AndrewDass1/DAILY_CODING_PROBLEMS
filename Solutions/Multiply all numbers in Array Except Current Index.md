# Directions
Given an array of integers, return a new array such that each element at index i of the new array is the product of all the numbers in the original array except the one at i. <br>
<br>
For example, if our input was [1, 2, 3, 4, 5], the expected output would be [120, 60, 40, 30, 24]. If our input was [3, 2, 1], the expected output would be [2, 3, 6]. <br>

## Procedure
1. Create a Function with a new list
```
def array_of_integers(list_of_numbers):
    new_list = []
```
2. Create a for loop within a for loop, that goes through each index of the list. An if statement is also implemented to not multiply the declared variable that saves the data by the current index the first loop is currently on.
```
def array_of_integers(list_of_numbers):
    new_list = []

    for i in range(0, len(list_of_numbers)):
        total_multiplication = 1
        for j in range(0, len(list_of_numbers)):
            if i != j:
                total_multiplication = total_multiplication * list_of_numbers[j]
            else:
                pass
```
3. Append the final result to the list and return the list when the code is finished executing
## Final Solution
```
def array_of_integers(list_of_numbers):
    new_list = []

    for i in range(0, len(list_of_numbers)):
        total_multiplication = 1
        for j in range(0, len(list_of_numbers)):
            if i != j:
                total_multiplication = total_multiplication * list_of_numbers[j]
            else:
                pass

            if j == len(list_of_numbers) - 1:
                    new_list.append(total_multiplication)

    return new_list

# Testing the Function
print(array_of_integers([5,6,7,8]))
```
