# 🧠 Problem 2: Running Sum of 1d Array

**LeetCode Link:**
🔗 [https://leetcode.com/problems/running-sum-of-1d-array](https://leetcode.com/problems/running-sum-of-1d-array)

---

## 🧩 Problem Description

Given an array `nums`. We define a running sum of an array as:

```
runningSum[i] = sum(nums[0]…nums[i])
```

Return the running sum of `nums`.

---

### 🧪 Examples with Input and Output

**Example 1:**

```
Input:
nums = [1,2,3,4]

Output:
[1,3,6,10]
```

**Example 2:**

```
Input:
nums = [1,1,1,1,1]

Output:
[1,2,3,4,5]
```

**Example 3:**

```
Input:
nums = [3,1,2,10,1]

Output:
[3,4,6,16,17]
```

---

## ✅ Constraints:

* `1 <= nums.length <= 1000`
* `-10^6 <= nums[i] <= 10^6`

---

## 🚀 Approach

### ✅ Intuition:

To compute the running sum, we just keep adding the current element to the cumulative sum so far.

---

## 🦀 Steps:

1. Initialize an empty list `result`
2. Initialize a variable `total = 0`
3. Loop through each element in `nums`
4. Add the element to `total`
5. Append `total` to `result`
6. Return `result`

---

### ⏱️ Time Complexity:

* **O(n)** — where `n` is the length of the array `nums`

---

### 🧠 Space Complexity:

* **O(n)** — for the output array

---

## 🧠 Edge Cases

* Array with only one element → running sum is the same as the element
* All negative numbers → should still work
* Very large positive/negative values → handled by Python's arbitrary precision
