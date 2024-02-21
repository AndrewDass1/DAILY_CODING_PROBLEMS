```
# On election day, a voting machine writes data in the form (voter_id, candidate_id) to a text file. 
# Write a program that reads this file as a stream and returns the top 3 candidates at any given time. If you find a voter voting more than once, report this as fraud.

def voting_machine(entries):

    voter_name_list = []
    voter_name_fraud_list = []

    candidate_name_list = {}

    for i in range(0, entries):
        voter_name = input("Enter voter name: ")
        candidate_name = input("Enter candidate name: ")

        if voter_name in voter_name_list:
            voter_fraud_name_list.append(voter_name)
        else:
            pass

        print(voter_name_list)

        if candidate_name not in candidate_name_list:
            candidate_name_list[voter_name] = 1
        else:
            candidate_name_list[voter_name] = candidate_name_list[voter_name] + 1

    return candidate_name_list, voter_name_fraud_list


print(voting_machine(3))
```
