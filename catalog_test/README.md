# Catalog based testiing

Document was created to get test cases for the simple functionality of an enemy object in a game. This was created as part of a group project in class. 

## Step 1 - Find elementary items

- preconditions: conditions that must be true before running the test
- postconditions: the result of running the test
- variables: inputs and ouputs the program operates on
- operations: calculations performed using the variables
- definitions: stuff the tester should know about the program

## Step 2 - Derive initial tests

- validated preconditions: simple ones (true/false) divide into two tests. complex ones (and/or) use mc/dc
- assumed preconditions: not necessary to check but should be checked elsewhere
- postcondition: has a conditional form, should be treated as validated
- definition: if it refers to variables and is in conditional form, treat as validated

## Step 3 - Complete using catalogs

common ones:

boolean
[in/out] true
[in/out] false

sequence
[in/out] empty
[in/out] 1 element
[in/out] more than 1
[in/out] max elements
[in] out of bounds
