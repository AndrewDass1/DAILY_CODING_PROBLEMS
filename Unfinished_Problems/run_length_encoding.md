# Directions
Run-length encoding is a fast and simple method of encoding strings. The basic idea is to represent repeated successive characters as a single count and character. For example, the string "AAAABBBCCDAA" would be encoded as "4A3B2C1D2A". <br>
<br>
Implement run-length encoding and decoding. You can assume the string to be encoded have no digits and consists solely of alphabetic characters. You can assume the string to be decoded is valid.

```
def successive_character_length(string_of_letters):
    number_counter = 0
    number_and_string_count = ""

    # len_of_the_string = len(string_of_letters) + 1

    for i in range(0, len(string_of_letters)):
        if i == 0:
            number_counter += 1
        elif i > 0:
            if string_of_letters[i] == string_of_letters[i-1]:
                number_counter += 1
            else:
                number_and_string_count += str(number_counter)
                number_and_string_count += string_of_letters[i-1]
                number_counter = 1


                print(number_and_string_count) # doesn't get the last letter
                # if statement below does

                if i == len(string_of_letters) - 1:
                    print("Final phase")

                    if string_of_letters[i] == string_of_letters[i-1]:
                        print("yes")
                        print(number_and_string_count)
                    else:
                        number_and_string_count += "1"
                        number_and_string_count += string_of_letters[i]
        else:
            print("Error")

    return number_and_string_count

# Test the function
successive_character_length("AAABCCD")
```
