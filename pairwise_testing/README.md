# Pairwise Testing

Helpful for designing tests for programs that have multiple parameters

## Example Program

An application that takes hamburger orders with the following inputs:

1. type of bun
   - sesame
   - non-sesame
2. number of patties
   - one
   - two
3. cheese
   - yes
   - no
4. side order
   - fries
   - onion rings
5. drink
   - soda
   - water
   - other
6. type of order
   - takeout
   - in house

## Number of possible tests

```
possible tests = 2 x 2 x 2 x 2 x 3 x 2
possible tests = 96
```

## Utilizing pairwise testing

#### Step 1
Start by ordering the parameters where the parameter with the most values is first and the one with the least values is last

```
drink, bun, patties, cheese, side, order
```

#### Step 2
Create a table and fill the first column with the first parameter's values two times each (two is the number of values of the next highest paramter)

```
drink  |  bun  |  patties  |  cheese  |  side  |  order
soda   |
soda   |
water  |
water  |
other  |
other  |
```

#### Step 3
Fill in second column where for each value of bun is assigned to each value of drink

```
drink  |  bun    |  patties  |  cheese  |  side  |  order
soda   |  sesame |
soda   |  none   |
water  |  sesame |
water  |  none   |
other  |  sesame |
other  |  none   |
```

#### Step 4
Fill in next column the same way as before but this time notice the combination sesame and two as well none and one are missing

```
drink  |  bun    |  patties  |  cheese  |  side  |  order
soda   |  sesame |  one      |
soda   |  none   |  two      |
water  |  sesame |  one      |
water  |  none   |  two      |
other  |  sesame |  one      |
other  |  none   |  two      |
```

Switch the second pair of values in patties

```
drink  |  bun    |  patties  |  cheese  |  side  |  order
soda   |  sesame |  one      |
soda   |  none   |  two      |
water  |  sesame |  two      |
water  |  none   |  one      |
other  |  sesame |  one      |
other  |  none   |  two      |
```

#### Step 5
Fill in the rest making sure to swap rows when necessary to get every combination

```
drink  |  bun    |  patties  |  cheese  |  side  |  order
soda   |  sesame |  one      |  yes     |  onion |  out
soda   |  none   |  two      |  no      |  fries |  in
water  |  sesame |  two      |  yes     |  fries |  out
water  |  none   |  one      |  no      |  onion |  in
other  |  sesame |  one      |  no      |  fries |  out
other  |  none   |  two      |  yes     |  onion |  in
```

#### Step 6
Missing combinations for (sesame,in) and (none,out). Can't swap any more rows since all the other rows have previously been swapped.
Insert two new rows for missing combinations.

```
drink  |  bun    |  patties  |  cheese  |  side  |  order
soda   |  sesame |  one      |  yes     |  onion |  out
soda   |  none   |  two      |  no      |  fries |  in
       |  sesame |           |          |        |  in
water  |  sesame |  two      |  yes     |  fries |  out
water  |  none   |  one      |  no      |  onion |  in
       |  none   |           |          |        |  out
other  |  sesame |  one      |  no      |  fries |  out
other  |  none   |  two      |  yes     |  onion |  in
```
