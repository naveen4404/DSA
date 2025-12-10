# DSA

# 💻 Coding Assessment Problems (Java)

This document contains clearly formatted coding problems (with examples) — ideal for practice or technical assessments.

---

## 🧩 Problem 1: Palindrome Partitioning – Min Cost  
**Difficulty:** 🟡 *Medium*

---

### 📝 Problem Statement
You are given a string **S**.  
You want to partition it into **at most K substrings** such that each substring is a **palindrome**.

Each substring has a **cost**:
- If a substring has length `L`, the cost is `L²` (squared length).
- There is **no additional cutting cost**.

Find the **minimum total cost** to partition `S` into **at most K palindromic substrings**.  
If it is impossible (i.e., if `K` is less than the minimum number of palindromes needed), return `-1`.

---

### 📥 Input Format
- The first line contains an integer **K**, the maximum number of palindrome substrings.  
- The second line contains a string **S**.

---

### 📤 Output Format
Print a single integer — the **minimum total cost**.

---

### 🔒 Constraints
- `1 ≤ K ≤ N`  
- `1 ≤ len(S) ≤ 500`  
- The string consists of lowercase Latin letters `a–z`.

---

### 🧪 Sample Test Cases

#### ✅ Sample Case 1
**Input:**

**Output:**

**Explanation:**  
The string can be split into 3 palindromes: “aa”, “bb”, “aa”.  
Each has cost `2² = 4`.  
Total cost = `4 + 4 + 4 = 12`.

---

#### ✅ Sample Case 2
**Input:**

**Output:**

**Explanation:**  
The entire string “racecar” is a palindrome of length 7.  
Cost = `7² = 49`.

---

## ⚙️ Problem 2: Deadline Rewards  
**Difficulty:** 🟢 *Easy-Medium*

---

### 📝 Problem Statement
You have **N tasks** waiting in a queue and a **single processor** that can handle **only one task at a time**.  

Every task `i` requires:
- `Tᵢ` units of processing time  
- Deadline `Dᵢ`  
- Reward `Rᵢ`  

If a task finishes by its deadline, you earn `Rᵢ`. Otherwise, you earn **nothing**.

Once a task starts, it must run to completion **without interruption**.  
You can choose the order of execution freely.  
The processor is idle at time 0, and all tasks are available immediately.

Find the **maximum total reward** you can earn.

---

### 💡 Note
- The reward from tasks does **not** depend on the start time — only on whether it finishes before its deadline.

---

### 📥 Input Format
- The first line contains an integer **N**, the number of tasks.  
- The next **N** lines each contain three integers:  
  `Tᵢ Dᵢ Rᵢ` — processing time, deadline, and reward.

---

### 📤 Output Format
Print a single integer — the **maximum total reward** achievable.

---

### 🔒 Constraints
- `1 ≤ N ≤ 1000`  
- `1 ≤ Tᵢ, Dᵢ, Rᵢ ≤ 2000`

---

### 🧪 Sample Test Cases

#### ✅ Sample Case 1
**Input:**

**Output:**

**Explanation:**  
We can first do Task 1, then Task 3.  
Both finish before their deadlines.  
Total reward = `10 + 12 = 22`.

---

#### ✅ Sample Case 2
**Input:**

**Output:**

---

## 🌟 Problem 3: Constellation Star Merging  
**Difficulty:** 🔵 *Medium-Hard*

---

### 📝 Problem Statement
You are given **N stars** arranged in a line from left to right.  
Each star has a **brightness value**.

You process the stars **strictly from left to right**.  
For each star, you may **connect it** or **skip it**.

When you connect star `i`:
- Every future star `j > i` whose brightness lies **strictly between**  
  `(brightness[i] / 2)` and `(brightness[i] × 2)` is **immediately merged** into a single virtual star.
- All merged stars are **removed permanently** and cannot be connected later.
- Only original, non-merged stars may be connected.
- Each successful connection counts as **+1**.

Find the **maximum number of individual connections** possible.

---

### 🧾 Notes
- The merging effect applies **only once** for each connection.  
- Merged stars are removed and do **not** trigger additional merges.

---

### 📥 Input Format
- The first line contains an integer **N**, the number of stars.  
- The next **N** lines each contain an integer representing `B[i]`, the brightness of each star.

---

### 📤 Output Format
Print a single integer — the **maximum number of connections**.

---

### 🔒 Constraints
- `1 ≤ N ≤ 200`  
- `1 ≤ B[i] ≤ 200`

---

### 🧪 Sample Test Cases

#### ✅ Sample Case 1
**Input:**

**Output:**

**Explanation:**  
Brightness: [45, 2, 9, 33, 22]  
Connect 45 → removes 33 and 22  
Connect 2 → removes none  
Connect 9 → removes none  
Connect 33, 22 → already removed  
Total connections = 4.

---

#### ✅ Sample Case 2
**Input:**

**Output:**

**Explanation:**  
Brightness: [5, 10, 30, 42, 34, 13, 20]  
Connect 5 → removes 10  
Connect 30 → removes 42, 34, 20  
Connect 13 → removes none  
Total connections = 4.

---

