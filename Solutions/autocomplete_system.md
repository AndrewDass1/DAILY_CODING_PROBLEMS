# Autocomplete System

## Directions
Implement an autocomplete system. That is, given a query string s and a set of all possible query strings, return all strings in the set that have s as a prefix. <br>
<br>
For example, given the query string de and the set of strings [dog, deer, deal], return [deer, deal].

## Procedure
1. Create a function that accepts two parameters: one for the prefix and a list that contains the words:
```
def check_prefix(prefix, list_of_words):
```
2. Create one variable that finds the length of the prefix and another variable that is an empty list
```
def check_prefix(prefix, list_of_words):
    length_of_prefix = len(prefix)

    list_of_words_with_prefix = []
```
3. A for loop will be used to go through the list of words to see if the prefix is in the beginning of each word that is in the list. If the prefix is in the word, it is then appended to the variable that has the empty list. The reason "prefix == list_of_words[i][0:length_of_prefix]" is list_of_words[i] searches through each index for each word and the second bracket that contains [0:length_of_prefix] slices each word to see if the suffix is in the beginning of each word. 

## Final Solution
```
def check_prefix(prefix, list_of_words):
    length_of_prefix = len(prefix)

    list_of_words_with_prefix = []

    for i in range(0, len(list_of_words)):
        if prefix == list_of_words[i][0:length_of_prefix]:
            list_of_words_with_prefix.append(list_of_words[i]) 
        else:
            pass

    return list_of_words_with_prefix

# Test the Function:
print(check_prefix("de", ["delaware", "destroy", "dog"]))
```
