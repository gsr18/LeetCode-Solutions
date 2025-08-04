# 🧠 Problem 1: Maximum Number of Words Found in Sentences

**LeetCode Link:**
🔗 [https://leetcode.com/problems/maximum-number-of-words-found-in-sentences](https://leetcode.com/problems/maximum-number-of-words-found-in-sentences)

---

## 🧩 Problem Description

A **sentence** is a list of words that are separated by a single space with no leading or trailing spaces.

You are given an array of strings `sentences`, where each `sentences[i]` represents a single sentence.

Return *the **maximum number of words** that appear in a single sentence*.

---

### 🧪 Examples with Input and Output

**Example 1:**

```
Input:
sentences = [
  "Alice and Bob love LeetCode",
  "I think so too",
  "This is great thanks very much"
]

Output:
6
```

**Example 2:**

```
Input:
sentences = [
  "Please wait",
  "Continue to fight",
  "Ready to go"
]

Output:
3
```

---

## ✅ Constraints:

* `1 <= sentences.length <= 100`
* `1 <= sentences[i].length <= 100`
* `sentences[i]` consists only of lowercase English letters and spaces.
* `sentences[i]` does **not** have leading or trailing spaces.
* All the words in `sentences[i]` are separated by a single space.

---

## 🚀 Approach

### ✅ Intuition:

Each sentence consists of words separated by spaces. So, the number of words in a sentence is the number of spaces + 1. We just need to loop through each sentence and track the maximum count.

---

## 🦀 Steps:

1. Initialize a variable `maxWords = 0`
2. Loop through each sentence in the array
3. For each sentence, count the number of spaces (using `count(' ')`)
4. Add 1 to get the number of words
5. Update `maxWords` if this count is greater than current `maxWords`
6. Return `maxWords`

---

### ⏱️ Time Complexity:

* **O(n \* m)** where:

  * `n` = number of sentences
  * `m` = average length of each sentence
* We scan every character in every sentence

---

### 🧠 Space Complexity:

* **O(1)** — we are using only a few variables to track the result

---

## 🧠 Edge Cases

* Sentence with only one word → should return 1
* Sentences with same number of words → returns any of them
* Very long sentence (up to 100 chars) → still works within constraints
* Sentence with exactly 100 words (i.e., 99 spaces) → handled efficiently
