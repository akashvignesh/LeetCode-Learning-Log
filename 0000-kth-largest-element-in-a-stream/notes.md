# 0000. Kth Largest Element in a Stream — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-kth-largest-element-in-a-stream.py)

---

## 🧠 Approach

Maintain a min-heap of size k. When adding a new element, if the heap size is less than k, add it. Otherwise, if the new element is larger than the smallest element in the heap (the root), remove the root and add the new element. The kth largest element is always the root of the min-heap.

---

## 💡 Step-by-Step Intuition

1. We want to find the kth largest element. This means we are interested in the top k elements. 
2. A min-heap is useful because it efficiently keeps track of the smallest element among a collection. 
3. If we maintain a min-heap of size k, the smallest element in this heap will be the kth largest element overall. 
4. When a new number comes, we compare it with the smallest element in our heap (the root). If the new number is larger, it has the potential to be among the top k, so we replace the smallest element with the new number. 
5. If the new number is smaller or equal, it cannot be the kth largest, so we ignore it. 
6. The heap size is capped at k, ensuring we only store the k largest elements seen so far.

---

## 🔑 Key Formula / Decision

```
N/A
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(log k) for add operation, as heap operations (push, pop) take logarithmic time with respect to the heap size (k). |
| Space | O(k) to store the k largest elements in the min-heap. |

---

## 🎯 Trick / Learning

Using a min-heap to find the kth largest element is counter-intuitive but efficient. The min-heap stores the k largest elements seen so far, and its root is the smallest among them, which is precisely the kth largest element.

---

## 📖 Revision Notes

- * Use a min-heap of size k to track the k largest elements.
- * The root of the min-heap is always the kth largest element.
- * Add new elements by comparing them to the heap's root and replacing if larger.

---

## 💻 Solution Code

```python
// solution not captured
```
