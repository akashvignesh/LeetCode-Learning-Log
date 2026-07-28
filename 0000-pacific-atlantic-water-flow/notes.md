# 0000. Pacific Atlantic Water Flow — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-pacific-atlantic-water-flow.py)

---

## 🧠 Approach

The solution uses two separate Depth First Search (DFS) traversals. One DFS starts from all cells adjacent to the Pacific Ocean and marks reachable cells. Another DFS starts from all cells adjacent to the Atlantic Ocean and marks reachable cells. The cells marked by both DFS traversals are the ones that can flow to both oceans.

---

## 💡 Step-by-Step Intuition

1. The problem asks for cells from which water can flow to both the Pacific and Atlantic oceans. 
2. Water flows from a cell to an adjacent cell if the adjacent cell's height is less than or equal to the current cell's height. 
3. Instead of checking flow from each cell to both oceans (which would be inefficient), we can reverse the problem: find cells reachable *from* the oceans. 
4. If a cell can reach the Pacific, it means water can flow *from* that cell to the Pacific. Conversely, if a cell is reachable *from* the Pacific (moving against the flow, i.e., to cells with greater or equal height), then water can flow *to* the Pacific from that cell. 
5. We perform two DFS traversals: one starting from all cells bordering the Pacific, and another from all cells bordering the Atlantic. 
6. During each DFS, we mark cells that can reach the respective ocean. 
7. The intersection of these two sets of marked cells gives us the final answer.

---

## 🔑 Key Formula / Decision

```
Condition for flow: `height[neighbor_row][neighbor_col] >= height[current_row][current_col]` (when moving from ocean inwards).
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(m*n) where m is the number of rows and n is the number of columns, because each cell is visited at most twice (once for Pacific DFS, once for Atlantic DFS). |
| Space | O(m*n) in the worst case for the recursion stack depth during DFS and for storing the visited sets. |

---

## 🎯 Trick / Learning

Reversing the problem by starting DFS from the oceans and moving inwards (to cells with greater or equal height) is a common and efficient technique for flow problems on grids.

---

## 📖 Revision Notes

- * Use DFS/BFS starting from ocean borders to find reachable cells.
- * The condition for moving inwards is `neighbor_height >= current_height`.
- * The final answer is the intersection of cells reachable from both oceans.

---

## 💻 Solution Code

```python
// solution not captured
```
