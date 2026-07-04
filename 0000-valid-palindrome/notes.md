# 0000. Valid Palindrome — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-valid-palindrome.py)

---

## 🧠 Approach

The solution first cleans the input string by removing non-alphanumeric characters and converting it to lowercase. Then, it uses two pointers, one starting from the beginning and the other from the end, to check if the cleaned string is a palindrome.

---

## 💡 Step-by-Step Intuition

1. A palindrome reads the same forwards and backward. 
2. To check this efficiently, we can ignore characters that don't contribute to the palindrome property (like spaces, punctuation) and case differences. 
3. After cleaning, we can compare characters from both ends inwards. If at any point the characters don't match, it's not a palindrome. If we reach the middle without mismatches, it is.

---

## 🔑 Key Formula / Decision

```
s[left] == s[right]
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(N) where N is the length of the string, because we iterate through the string once for cleaning and at most once for the two-pointer comparison. |
| Space | O(N) in the worst case, due to the creation of a new string for the cleaned version. If modifying in-place was allowed and feasible, it could be O(1). |

---

## 🎯 Trick / Learning

The key trick is to preprocess the string to handle case insensitivity and ignore irrelevant characters before applying the core palindrome check logic.

---

## 📖 Revision Notes

- * Preprocess string: lowercase and alphanumeric only.
- * Use two pointers (start and end) moving inwards.
- * If characters at pointers mismatch, return False. If pointers meet/cross, return True.

---

## 💻 Solution Code

```python
// solution not captured
```
