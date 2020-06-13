# Modified Condition/Decision Coverage

In a compound conditional statement, each term of the compound conditional must be tested in true and false states in two separate test cases, in which all other conditionals are identical between the two cases, and in which the conditional which changes affects the outcome of the decision

## example
```
if((a || b) && c)
return true;
else
return false;
```
