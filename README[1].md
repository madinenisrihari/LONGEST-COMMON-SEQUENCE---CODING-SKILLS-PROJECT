# Longest Common Subsequence (LCS) Project in C++

## 📌 Project Overview
This project implements the **Longest Common Subsequence (LCS)** algorithm using Dynamic Programming in C++.

The LCS problem finds the longest subsequence common to two strings.

---

## 👨‍💻 Group Members

- Shaik Asif Roshan - AP24110011881  
- M. Sri Hari - AP24110011855  
- V. Swammy - AP24110011868  
- Md. Afrid - AP24110011860  
- Shaik Ismail - AP24110011823  

---

## 🧠 Concept Explanation

### What is LCS?
The Longest Common Subsequence is the longest sequence that appears in the same order in both strings but not necessarily contiguous.

Example:
```
Input:
s1 = "ABCBDAB"
s2 = "BDCAB"

Output:
LCS = "BCAB"
Length = 4
```

---

## ⚙️ Algorithm Used

We use **Dynamic Programming (DP)** to solve this problem efficiently.

### Steps:
1. Create a DP table of size (m+1) x (n+1)
2. Fill the table using:
   - If characters match → add 1
   - Else → take max of left or top
3. Backtrack to find the LCS string

---

## 📊 Time & Space Complexity

- Time Complexity: O(m × n)
- Space Complexity: O(m × n)

---

## 🧾 Code Explanation

### 1. Input
We take two strings from the user.

### 2. DP Table Creation
```
vector<vector<int>> dp(m + 1, vector<int>(n + 1, 0));
```

### 3. Filling DP Table
- If characters match:
```
dp[i][j] = 1 + dp[i-1][j-1];
```
- Else:
```
dp[i][j] = max(dp[i-1][j], dp[i][j-1]);
```

### 4. Finding LCS String
We backtrack from dp[m][n] to construct the LCS string.

---

## ▶️ How to Run

### Compile:
```
g++ main.cpp -o lcs
```

### Run:
```
./lcs
```

---

## 📌 Sample Input/Output

```
Enter first string: ABCDGH
Enter second string: AEDFHR

Length of LCS: 3
LCS String: ADH
```

---

## 📚 Applications

- DNA sequence analysis
- Version control (diff tools)
- Spell checking
- Data comparison

---

## ✅ Conclusion
This project demonstrates how dynamic programming can efficiently solve complex problems like LCS.

