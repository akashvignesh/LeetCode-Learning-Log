# 0000. Valid Sudoku — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-valid-sudoku.py)

---

## 🧠 Approach

The solution iterates through the Sudoku board and uses sets to keep track of seen numbers in rows, columns, and 3x3 subgrids. If a duplicate is found in any of these structures, the board is invalid.

---

## 💡 Step-by-Step Intuition

1. A valid Sudoku must satisfy three conditions: each row contains unique digits 1-9, each column contains unique digits 1-9, and each of the nine 3x3 sub-boxes of the grid contains unique digits 1-
9. 
2. We can use hash sets (or dictionaries) to efficiently check for duplicates. 
3. We need to maintain separate sets for each row, each column, and each 3x3 sub-box. 
4. Iterate through each cell of the 9x9 board. For each cell containing a digit: check if it's already in the set for its row, its column, and its corresponding 3x3 sub-box. If it is, return False. Otherwise, add the digit to all three relevant sets. 
5. If the iteration completes without finding any duplicates, return True.

---

## 🔑 Key Formula / Decision

```
For each cell (r, c) with digit d: check if d is in row_sets[r], col_sets[c], or box_sets[box_index(r, c)]. If yes, invalid. Else, add d to all three.
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(1) - The board size is fixed at 9x9, so the number of operations is constant regardless of input. |
| Space | O(1) - The space used by the sets is proportional to the board size, which is fixed at 9x9, hence constant. |

---

## 🎯 Trick / Learning

The key trick is to efficiently map a cell's row and column index to its corresponding 3x3 sub-box index. This can be done using integer division: `box_index = (row // 3) * 3 + (col // 3)`.

---

## 📖 Revision Notes

- * Use sets for O(1) average time complexity lookups to detect duplicates.
- * Remember to check rows, columns, and 3x3 sub-boxes independently.
- * The mapping to 3x3 sub-boxes is crucial and can be calculated using integer division.

---

## 💻 Solution Code

```python
// solution not captured
```
