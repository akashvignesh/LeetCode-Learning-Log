# 0213. House Robber II

## Difficulty
Medium

## Topic / Pattern
Dynamic Programming, Array

## Language
Python

## Approach
The problem is a variation of House Robber I, with the constraint that the first and last houses are adjacent. This means we cannot rob both. We can solve this by considering two scenarios: robbing houses 1 to n-1, and robbing houses 2 to n. The maximum of these two scenarios will be the answer.

## Intuition
1. The core problem is to find the maximum amount of money that can be robbed from a linear arrangement of houses without robbing adjacent ones. This is the classic House Robber I problem. 2. The twist here is that the first and last houses are considered adjacent, meaning we cannot rob both. 3. This implies two mutually exclusive possibilities: either we rob the first house (and thus cannot rob the last), or we don't rob the first house (and thus can potentially rob the last). 4. Therefore, we can break the problem into two subproblems: a) Find the maximum amount robbing houses from index 0 to n-2 (excluding the last house). b) Find the maximum amount robbing houses from index 1 to n-1 (excluding the first house). 5. The final answer is the maximum of the results from these two subproblems. 6. A base case for a single house is that we can rob it.

## Key Formula / Decision
max(robRange(nums[:-1]), robRange(nums[1:])) where robRange(arr) is the solution to House Robber I on arr.

## Complexity
- Time Complexity: O(N) because we call the House Robber I solution twice, and each call takes O(N) time.
- Space Complexity: O(1) because the House Robber I solution uses constant extra space (only a few variables to store previous DP states).

## LeetCode Submission Result
- Runtime: undefined (3.03%)
- Memory: 19432000 (10.72%)

## Trick / Learning
The key trick is to realize that the circular dependency (first and last houses being adjacent) can be broken by considering two linear subproblems that cover all valid combinations.

## Revision Notes
* Handle the circular constraint by splitting into two linear problems: robbing up to n-1, and robbing from 1 to n. * The core logic is the same as House Robber I (DP with two states: rob current or skip current). * Remember the edge case of a single house.

## Solution File
[View Solution](./0213-house-robber-ii.py)
