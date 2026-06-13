# 0000. Evaluate Reverse Polish Notation — AI Analysis

[⬅ Problem](./README.md) &nbsp;·&nbsp; [💻 Code](./0000-evaluate-reverse-polish-notation.py)

---

## 🧠 Approach

The solution uses a stack to evaluate the Reverse Polish Notation (RPN) expression. When a number is encountered, it's pushed onto the stack. When an operator is encountered, the top two numbers are popped, the operation is performed, and the result is pushed back onto the stack.

---

## 💡 Step-by-Step Intuition

1. Reverse Polish Notation (RPN) is a postfix notation where operators follow their operands. 
2. A stack is a natural data structure for evaluating RPN because it allows us to store operands until an operator is encountered. 
3. When we see a number, we push it onto the stack. 
4. When we see an operator, we pop the last two numbers from the stack (which are the operands for that operator), perform the operation, and push the result back onto the stack. 
5. After processing the entire expression, the final result will be the only element left on the stack.

---

## 🔑 Key Formula / Decision

```
operand2 = stack.pop(); operand1 = stack.pop(); result = perform_operation(operand1, operand2); stack.push(result);
```

---

## ⏱ Complexity

| | Complexity |
|---|---|
| Time  | O(N) where N is the number of tokens in the input array, as each token is processed exactly once. |
| Space | O(N) in the worst case, where N is the number of tokens, as the stack can store up to N/2 numbers if the expression is structured like `num num op num num op ...`. |

---

## 🎯 Trick / Learning

The order of popping operands matters for subtraction and division. The second number popped is the first operand, and the first number popped is the second operand.

---

## 📖 Revision Notes

- * Use a stack to process RPN expressions.
- * Push numbers onto the stack, pop two for operators, and push the result.
- * Be mindful of operand order for non-commutative operations (subtraction, division).

---

## 💻 Solution Code

```python
// solution not captured
```
