# 0020. Valid Parentheses

**Difficulty:** Easy &nbsp;|&nbsp; **Language:** Python &nbsp;|&nbsp; **Date:** 2026-06-12

[🔗 LeetCode](https://leetcode.com/problems/valid-parentheses/) &nbsp;·&nbsp; [💻 Code](./0020-valid-parentheses.py) &nbsp;·&nbsp; [🧠 AI Analysis](./notes.md)

---

## 📊 Submission Performance

| Metric | Result | Percentile |
|--------|--------|------------|
| 🚀 Runtime | 0 ms | Beats 100.00% |
| 🧠 Memory  | 19.3 MB  | Beats 67.42%  |

---

## 📋 Problem Description

Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

An input string is valid if:


	Open brackets must be closed by the same type of brackets.
	Open brackets must be closed in the correct order.
	Every close bracket has a corresponding open bracket of the same type.


 
Example 1:


Input: s = "()"

Output: true


Example 2:


Input: s = "()[]{}"

Output: true


Example 3:


Input: s = "(]"

Output: false


Example 4:


Input: s = "([])"

Output: true


Example 5:


Input: s = "([)]"

Output: false


 
Constraints:


	1 <= s.length <= 104
	s consists of parentheses only '()[]{}'.
