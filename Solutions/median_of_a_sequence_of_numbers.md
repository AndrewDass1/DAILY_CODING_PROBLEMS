# Finding the Medians of a Sequence of Numbers

## Directions
Compute the running median of a sequence of numbers. That is, given a stream of numbers, print out the median of the list so far on each new element. <br>
<br>
Recall that the median of an even-numbered list is the average of the two middle numbers. <br>
<br>
For example, given the sequence [2, 1, 5, 7, 2, 0, 5], your algorithm should print out: <br>
```
2
1.5
2
3.5
2
2
2
```
## Procedure
1. Create a function that asks how many numbers will be inputted into the list:
```
def sequence_of_numbers():
    how_many_numbers = int(input("How many numbers: "))
```
2. Three variables will be created: one with an empty list that will contain the inputted number values from "how_many_numbers", another variable to sort the list of inputted number values to calculate the median value, and another list data type that contains the calculated median values. The variable names in this script are "list_of_numbers", "calculate_median" and "medians".  
```
def sequence_of_numbers():
    how_many_numbers = int(input("How many numbers: "))

    list_of_numbers = []

    calculate_median = sorted(list_of_numbers)

    medians = []
```
3. Create a for-loop and specify the range is from 0 and the ending is "how_many_numbers". This will allow how many numbers that were specified to be entered into the list by appending the values to it. For each iteration of the for-loop, the list is also sorted and the length of the list is taken accounted for to calcuate the median each time.
```
def sequence_of_numbers():
    how_many_numbers = int(input("How many numbers: "))

    list_of_numbers = []

    calculate_median = sorted(list_of_numbers)

    medians = []

    for i in range(0, how_many_numbers):
        enter_number_in_list = int(input("Enter a number: "))
        list_of_numbers.append(enter_number_in_list)

        list_of_numbers = sorted(list_of_numbers)

        length_of_numbers = len(list_of_numbers)
```
4. Depending on the length of the list, an if-elif-else statement was implemented to calcuate the median. <br> <br>
If the length of the list is 1, then the median is the only value that is in the list. <br> <br>
If the length of the list is 2, then the median is the average of the two values present in the list. <br> <br>
If the length of the list has more than two values and has an odd amount of values, the index that contains the median can be calculated by dividing the length of the list by 2. If the length of the list is an odd number, dividing the length gives a decimal value. The decimal can then be subtracted by 0.5, and this new number is the index that contains the median value. The calculated index has to be casted from a float to an integer to prevent any errors. <br> <br>
If the length of the list is has more than two values and has an even amount of values, the average of the two middle values must be calculated. To find the two indices that are the middle numbers, the length of the list must be divided by 2. Dividing the list by 2 gives the index of the higher value and to calculate the average and the lower value can be found by subtracting 1 from the dividing the list's length by 1. The average is then taken from those two indices. <br> <br> 
## Final Script
```
def sequence_of_numbers():
    how_many_numbers = int(input("How many numbers: "))

    list_of_numbers = []

    calculate_median = sorted(list_of_numbers)

    medians = []

    for i in range(0, how_many_numbers):
        enter_number_in_list = int(input("Enter a number: "))
        list_of_numbers.append(enter_number_in_list)
        list_of_numbers = sorted(list_of_numbers)

        length_of_numbers = len(list_of_numbers)

        if length_of_numbers == 1:
            calculate_median = list_of_numbers[0]
            medians.append(calculate_median)

        elif length_of_numbers == 2:
            calculate_median = (list_of_numbers[0] + list_of_numbers[1] ) / 2
            medians.append(calculate_median)

        elif length_of_numbers >=3 and length_of_numbers % 2 == 1:
            find_middle_position = length_of_numbers / 2
            odd_median_index = find_middle_position - 0.5
            odd_median_index = int(odd_median_index)

            medians.append(list_of_numbers[odd_median_index])
        elif length_of_numbers >=3 and length_of_numbers % 2 == 0:
            find_middle_position = length_of_numbers / 2

            lower_half = int(find_middle_position - 1)

            upper_half = int(find_middle_position)

            calculate_median = (list_of_numbers[lower_half] + list_of_numbers[upper_half]) / 2

            medians.append(calculate_median)
        else:
            print("Error occurred. Rerun the program again.")
            break

    return medians

print(sequence_of_numbers())
```
