# 🧠 Problem 5: Defanging an IP Address

**LeetCode Link:**
🔗 [https://leetcode.com/problems/defanging-an-ip-address](https://leetcode.com/problems/defanging-an-ip-address)

---

## 🧩 Problem Description

Given a valid (IPv4) IP `address`, return a defanged version of that IP address.

A defanged IP address replaces every period `.` with `[.]`.

---

### 🧪 Examples with Input and Output

**Example 1:**

```
Input:
address = "1.1.1.1"

Output:
"1[.]1[.]1[.]1"
```

**Example 2:**

```
Input:
address = "255.100.50.0"

Output:
"255[.]100[.]50[.]0"
```

---

## ✅ Constraints:

* The given `address` is a valid IPv4 address.
* Address length: `7 <= address.length <= 15`
* Each segment between `.` is a valid decimal between 0–255

---

## 🚀 Approach

### ✅ Intuition:

Since all we need to do is replace `.` with `[.]`, we can either:

1. Use Python's built-in string method `.replace()`
2. Or manually build the new string character by character (for educational purpose)

---

## 🦀 Steps:

### Approach 1: Using `.replace()`

```python
return address.replace('.', '[.]')
```

### Approach 2: Manual String Build

```python
def defangIPaddr(address: str) -> str:
    result = ""
    for char in address:
        if char == ".":
            result += "[.]"
        else:
            result += char
    return result
```

---

### ⏱️ Time Complexity:

* **O(n)** — where `n` is the length of the string

---

### 🧠 Space Complexity:

* **O(n)** — since we’re building a new string

---

## 🧠 Edge Cases

* IP with all segments same (e.g., "0.0.0.0") → all periods must be replaced
* No period → Not possible per problem constraints (but if it was, string remains same)
* Longest valid IP (e.g., "255.255.255.255") → handled easily

---

## 🔁 Pattern:

🧵 **String Manipulation**

* Replacing characters
* Building strings from characters

📦 **Tools used:**

* String methods (`replace()`)
* Looping through strings
* Conditional character transformation
