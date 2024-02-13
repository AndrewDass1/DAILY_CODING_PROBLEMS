```
# The power set of a set is the set of all its subsets. Write a function that, given a set, generates its power set.

# For example, given the set {1, 2, 3}, it should return {{}, {1}, {2}, {3}, {1, 2}, {1, 3}, {2, 3}, {1, 2, 3}}

def make_power_set(the_set):

    set_of_values = set()

    for i in range(0, len(the_set)):
        set_of_values.add(i)

    for i2 in range(0, len(the_set)):
        for j in range(0, len(the_set)):
            if i2 != j:
                pass
            else:
                set_of_values.add((set_of_values[i2], set_of_values[j]))

    # set_of_values.add(tuple(set_of_values))

    return set(set_of_values)

    
print(make_power_set({1, 2, 3}))
```
