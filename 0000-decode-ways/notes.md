# 0000. Decode Ways — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-decode-ways.py)

---

## 🧠 Approach

This problem can be solved using dynamic programming. We define dp[i] as the number of ways to decode the substring s[0...i-1]. We iterate through the string and calculate dp[i] based on the previous values dp[i-1] and dp[i-2].

---

## 💡 Step-by-Step Intuition

1. The problem asks for the number of ways to decode a string of digits into letters. Each digit maps to a letter (1->A, 2->B, ..., 26->Z). 
2. A single digit can be decoded if it's not '0'. 
3. Two digits can be decoded if they form a number between 10 and 26 inclusive. 
4. We can use dynamic programming where dp[i] represents the number of ways to decode the first i characters of the string. 
5. The base cases are dp[0] = 1 (empty string has one way to be decoded) and dp[1] depends on the first character. 
6. For dp[i], we consider the last digit s[i-1] and the last two digits s[i-2]s[i-1]. If s[i-1] is a valid single digit, we add dp[i-1] to dp[i]. If s[i-2]s[i-1] form a valid two-digit number, we add dp[i-2] to dp[i].

---

## 🔑 Key Formula / Decision

```
dp[i] = (dp[i-1] if s[i-1] is valid single digit) + (dp[i-2] if s[i-2]s[i-1] is valid two-digit number)
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(n) because we iterate through the string once to fill the DP table. |
| Space | O(n) because we use a DP array of size n+1 to store intermediate results. |

---

## 🎯 Trick / Learning

Be careful with leading zeros and the edge cases for single and double-digit decodings. The base case dp[0] = 1 is crucial for the logic to work correctly.

---

## 📖 Revision Notes

- * Use DP to count decoding ways, where dp[i] is ways to decode s[:i].
- * Consider single-digit (s[i-1]) and two-digit (s[i-2:i]) decodings for transitions.
- * Handle '0' carefully: '0' alone is invalid, '10'-'26' are valid two-digit decodings.

---

## 💻 Solution Code

```python
// solution not captured
```
