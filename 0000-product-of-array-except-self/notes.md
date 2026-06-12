# 0000. Product of Array Except Self — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-product-of-array-except-self.py)

---

## 🧠 Approach

The solution calculates the product of all elements to the left of each element and the product of all elements to the right of each element in two separate passes. The final result for each element is the product of its corresponding left and right products.

---

## 💡 Step-by-Step Intuition

1. For each element at index i, we need the product of all elements before i and the product of all elements after i. 
2. We can compute the prefix products (product of elements from the beginning up to index i-1) in one pass. 
3. We can compute the suffix products (product of elements from the end down to index i+1) in another pass. 
4. The final answer for index i is the product of the prefix product at i and the suffix product at i.

---

## 🔑 Key Formula / Decision

```
result[i] = prefix_product[i] * suffix_product[i]
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(n) because we iterate through the array three times (once for prefix products, once for suffix products, and once to combine them). |
| Space | O(n) because we use two additional arrays to store prefix and suffix products. (Note: The problem statement often allows O(1) extra space if the output array doesn't count towards space complexity, which can be achieved by modifying the result array in place during the passes.) |

---

## 🎯 Trick / Learning

The key trick is to avoid division. By calculating prefix and suffix products separately, we can achieve the desired result without needing to compute the total product and then divide, which would fail if the array contains zeros.

---

## 📖 Revision Notes

- * Calculate prefix products from left to right.
- * Calculate suffix products from right to left.
- * Multiply corresponding prefix and suffix products to get the final answer.

---

## 💻 Solution Code

```python
// solution not captured
```
