🧠 Problem 4: Shuffle the Array

LeetCode Link:
🔗 https://leetcode.com/problems/shuffle-the-array

🧩 Problem Description

Given the array nums consisting of 2n elements in the form:

[x1,x2,...,xn,y1,y2,...,yn]

Return the array in the form:

[x1,y1,x2,y2,...,xn,yn]

🧪 Examples with Input and Output

Example 1:

Input: nums = [2,5,1,3,4,7], n = 3
Output: [2,3,5,4,1,7]

Example 2:

Input: nums = [1,2,3,4,4,3,2,1], n = 4
Output: [1,4,2,3,3,2,4,1]

Example 3:

Input: nums = [1,1,2,2], n = 2
Output: [1,2,1,2]

✅ Constraints:

1 <= n <= 500

nums.length == 2 * n

1 <= nums[i] <= 10^3

🚀 Approach

✅ Intuition:

We need to interleave the first n elements (x's) with the second n elements (y's).

🦀 Steps:

Initialize an empty list result

Loop from i = 0 to n - 1

In each iteration:

Append nums[i] (x)

Append nums[i + n] (y)

Return result

⏱️ Time Complexity:

O(n) — One pass through the input array of length 2n

🧠 Space Complexity:

O(n) — New array of size 2n created

🧠 Edge Cases

All elements are the same: should still return valid interleaving

Minimum size input (n = 1) like [1,2] ➔ [1,2]

Inputs with max values like 1000

🔄 Pattern:

This problem belongs to the Two Pointers / Index Manipulation category. You are splitting and recombining arrays with known rules. Very common in array manipulation and merge-style logic.

