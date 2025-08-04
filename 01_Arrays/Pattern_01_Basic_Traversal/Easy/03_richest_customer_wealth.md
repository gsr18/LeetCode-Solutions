# 🧠 Problem 3: Richest Customer Wealth

**LeetCode Link:**
🔗 [https://leetcode.com/problems/richest-customer-wealth](https://leetcode.com/problems/richest-customer-wealth)

---

## 🧩 Problem Description

You are given an `m x n` integer grid `accounts` where `accounts[i][j]` is the amount of money the `iᵗʰ` customer has in the `jᵗʰ` bank. Return *the wealth that the richest customer has.*

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.

---

### 🧪 Examples with Input and Output

**Example 1:**

```
Input:
accounts = [[1,2,3],[3,2,1]]

Output:
6

Explanation:
1st customer has wealth = 1 + 2 + 3 = 6
2nd customer has wealth = 3 + 2 + 1 = 6
Maximum wealth = max(6, 6) = 6
```

**Example 2:**

```
Input:
accounts = [[1,5],[7,3],[3,5]]

Output:
10

Explanation:
1st customer has wealth = 1 + 5 = 6
2nd customer has wealth = 7 + 3 = 10
3rd customer has wealth = 3 + 5 = 8
Maximum wealth = max(6, 10, 8) = 10
```

**Example 3:**

```
Input:
accounts = [[2,8,7],[7,1,3],[1,9,5]]

Output:
17
```

---

## ✅ Constraints:

* `m == accounts.length`
* `n == accounts[i].length`
* `1 <= m, n <= 50`
* `1 <= accounts[i][j] <= 100`

---

## 🚀 Approach

### ✅ Intuition:

We are asked to find the *maximum total wealth* among all customers. Each row in the `accounts` matrix represents one customer and contains all of their bank balances. We just need to:

* Compute the sum of each row (each customer's total wealth)
* Keep track of the maximum among these sums

---

## 🦀 Steps:

1. Initialize a variable `max_wealth = 0`
2. Loop through each customer (each row in `accounts`):

   * Compute the sum of that row → `wealth = sum(customer)`
   * Update `max_wealth = max(max_wealth, wealth)`
3. Return `max_wealth`

---

### ⏱️ Time Complexity:

* **O(m × n)** — We go through each element in the matrix

---

### 🧠 Space Complexity:

* **O(1)** — No extra space used other than a few variables

---

## 🧠 Edge Cases

* All accounts have the same total → still return the correct maximum
* Only one customer → just return their wealth
* All values are equal → sum will depend only on count of banks per customer

---
