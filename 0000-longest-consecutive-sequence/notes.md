# 0000. Longest Consecutive Sequence — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-longest-consecutive-sequence.py)

---

## 🧠 Approach

The solution uses a hash set to store all numbers for efficient lookups. It then iterates through the numbers, and for each number, it checks if it's the start of a consecutive sequence by verifying if the previous number is not present in the set. If it is a start, it extends the sequence as far as possible and updates the maximum length.

---

## 💡 Step-by-Step Intuition

1. Store all numbers in a hash set for O(1) average time complexity lookups. 
2. Iterate through each number in the input array. 
3. For each number, check if it's the potential start of a consecutive sequence. A number is a start if `num - 1` is NOT present in the hash set. 
4. If it's a start, then find the length of the consecutive sequence starting from this number by repeatedly checking for `num + 1`, `num + 2`, etc., in the hash set. 
5. Keep track of the maximum length found so far. 
6. Return the maximum length.

---

## 🔑 Key Formula / Decision

```
max_length = max(max_length, current_length)
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(n) because each number is inserted into the hash set once and each number is visited at most twice (once in the outer loop and once in the inner while loop if it's part of a sequence). |
| Space | O(n) to store all the numbers in the hash set. |

---

## 🎯 Trick / Learning

The key trick is to only start counting a consecutive sequence when you encounter the *smallest* number in that sequence (i.e., when `num - 1` is not in the set). This avoids redundant checks and ensures each number is processed efficiently.

---

## 📖 Revision Notes

- * Use a hash set for O(1) average time lookups.
- * Optimize by only starting sequence checks from the smallest element of a potential sequence.
- * The algorithm's efficiency relies on avoiding re-processing numbers that are part of already-checked sequences.

---

## 💻 Solution Code

```python
// solution not captured
```
