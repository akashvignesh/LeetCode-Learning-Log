# 0000. Last Stone Weight — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-last-stone-weight.py)

---

## 🧠 Approach

The problem can be solved by repeatedly finding the two heaviest stones, smashing them together, and putting the result back into the collection. A max-heap (priority queue) is an efficient data structure for this, as it allows quick retrieval of the maximum elements.

---

## 💡 Step-by-Step Intuition

1. We want to always pick the two largest stones. 
2. A max-heap is perfect for this, as it keeps the largest element at the top. 
3. We can simulate the process: extract the two largest, calculate the difference, and if the difference is non-zero, insert it back. 
4. Repeat until at most one stone remains.

---

## 🔑 Key Formula / Decision

```
if y >= x: new_stone = y - x else: new_stone = x - y (where x and y are the two largest stones)
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(N log N) - Building the heap takes O(N), and each of the N-1 smash operations involves two heap extractions (O(log N)) and potentially one heap insertion (O(log N)). |
| Space | O(N) - The heap stores all N stones initially. |

---

## 🎯 Trick / Learning

Using a max-heap (priority queue) is crucial for efficiency. Without it, repeatedly sorting the list would lead to a much slower O(N^2 log N) or O(N^2) solution.

---

## 📖 Revision Notes

- * Use a max-heap to efficiently find the two largest stones.
- * The core operation is extracting two max elements, calculating the difference, and re-inserting if non-zero.
- * The process stops when the heap has 0 or 1 element.

---

## 💻 Solution Code

```python
// solution not captured
```
