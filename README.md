# 60_wrapBinarySearch

## Recall inverse functions and logarithms

What is meant by y = log<sub>2</sub>x? What does its graph look like?

The mathematical equation y = log<sub>2</sub>x is the same as the equation x = 2<sup>y</sup>. Logarithms are the inverse of exponentiation.


![Image of Graph](https://people.richland.edu/james/lecture/m116/logs/log2.gif)

## Description of recursive solution

### Statement of Problem

Given an Integer *i* and an ordered list of Integers, determine the index number where *i* appears in the list, or if it doesn't appear at all.

### Statement of the recursive abstraction

Given an Integer *i* and an ordered list of Integers of length *n*, the recursive abstraction can determine the index where *i* appears in an ordered list of Integers of length half of the original list.

### Parts of the solution

0. Boolean expression determining whether to use base case or recursive case
```
if (low >= high)
```
1. Solution to Base Case
```
return -1;
```
2. Solution to Recursive Cases
- leftover

- recursive abstraction

- combiner
```
    if (list_iAS.get(current) == findMe) return current;
    else if (list_iAS.get( current) < findMe) {
	return indexOf_recursive(findMe, current + 1, high);
    }
    else {
	return indexOf_recursive(findMe, low, current);
    }