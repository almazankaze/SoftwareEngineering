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

## Step 1

Start by ordering the parameters where the parameter with the most values is first and the one with the least values is last

```
drink, bun, patties, cheese, side, order
```
