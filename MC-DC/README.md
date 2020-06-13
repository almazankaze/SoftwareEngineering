# Modified Condition/Decision Coverage

In a compound conditional statement, each term of the compound conditional must be tested in true and false states in two separate test cases, in which all other conditionals are identical between the two cases, and in which the conditional which changes affects the outcome of the decision

## example
```
if(a && b && c)
return true;
else
return false;
```

### possible combinations
```
test |  a  |  b  |  c  |  result  
1    |  0  |  0  |  0  |  0
2    |  0  |  0  |  1  |  0
3    |  0  |  1  |  0  |  0
4    |  0  |  1  |  1  |  0
5    |  1  |  0  |  0  |  0
6    |  1  |  0  |  1  |  0
7    |  1  |  1  |  0  |  0
8    |  1  |  1  |  1  |  1
```

- test 4 and 8 shows a independantly affect outcome
- test 6 and 8 show b independantly affect outcome
- test 7 and 8 shows c independantly affect outcome

keep tests 4, 6, 7, 8. The others are redundant
```
test |  a  |  b  |  c  |  result  
1    |  0  |  1  |  1  |  0
2    |  1  |  0  |  1  |  0
3    |  1  |  1  |  0  |  0
4    |  1  |  1  |  1  |  1
```
