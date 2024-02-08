# Implement a Job Scheduler

## Problem
Implement a job scheduler which takes in a function f and an integer n, and calls f after n milliseconds.

## Procedure
1. Import the time module. Later in the program, the method "time.sleep()" is used to delay the function for the amount of milliseconds.
```
import time
```
2. Before creating the function, declare a variable that takes a number. This number will be used as the numeric input for the "time.sleep()" function :
```
import time

enter_seconds_number = int(input("Enter number in seconds (which is then converted to milliseconds to delay function): "))
```
3. Create the function f, that takes a variable n:
```
import time

enter_seconds_number = int(input("Enter number in seconds (which is then converted to milliseconds to delay function): "))

def f(n):
```
4. "time.sleep()" takes a numerical input, to delay running any process in the function by the amount of seconds. In the function, the variable n contains the number input in seconds, which is then converted to milliseconds, and the converted variable is used in the "time.sleep()" input:
## Final Solution
```
import time

enter_seconds_number = int(input("Enter number in seconds (which is then converted to milliseconds to delay function): "))

def f(n):
    milliseconds_conversion = n * 0.001
    print("Amount of milliseconds delay:", milliseconds_conversion)
    time.sleep(milliseconds_conversion)

# Calling the Function:
f(enter_seconds_number)
```
