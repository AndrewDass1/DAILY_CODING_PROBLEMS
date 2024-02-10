```
# Exercise 13

# Given an integer k and a string s, find the length of the longest substring that contains at most k distinct characters.

# For example, given s = "abcba" and k = 2, the longest substring with k distinct characters is "bcb".

# string is s
# integer is k

def longest_distinct_characters(s, k):
    letter_check = ""

    for i in range(0, len(s)):
        if s[i] not in letter_check:
            letter_check += s[i]

        if len(letter_check) = k
    
    return letter_check

# then you need to print the index of the word as it is
# use a while loop? reexecute the function if it does not work

longest_distinct_characters("word", 3)
```
