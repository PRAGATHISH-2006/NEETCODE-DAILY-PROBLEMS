# 🧩 NeetCode Daily Solutions

📅 **Date:** 2026-03-10 &nbsp;|&nbsp; ✅ **Problems Solved: 3** &nbsp;|&nbsp; 🏷️ **Topics:** Arrays, Strings

---

### 1. Valid Anagram
**Difficulty:** 🟢 Easy &nbsp;|&nbsp; **Topic:** String

#### ✅ Solution (Java)
```java
class Solution {
    public boolean isAnagram(String s, String t) {
        int a[] = new int[26];
        if (s.length() != t.length()) return false;
        for (char b : s.toCharArray()) {
            a[b - 'a']++;
        }
        for (char b : t.toCharArray()) {
            a[b - 'a']--;
        }
        for (int i = 0; i < t.length(); i++) {
            if (a[t.charAt(i) - 'a'] != 0) return false;
        }
        return true;
    }
}
```

---

### 2. Replace Elements with Greatest Element on Right Side
**Difficulty:** 🟢 Easy &nbsp;|&nbsp; **Topic:** Array

#### ✅ Solution (Java)
```java
class Solution {
    public int[] replaceElements(int[] a) {
        for (int i = 0; i < a.length; i++) {
            int max = 0;
            for (int j = i + 1; j < a.length; j++) {
                if (a[j] > max) max = a[j];
            }
            a[i] = max;
        }
        a[a.length - 1] = -1;
        return a;
    }
}
```

---

### 3. Is Subsequence
**Difficulty:** 🟢 Easy &nbsp;|&nbsp; **Topic:** Two Pointers, String

#### ✅ Solution (Java)
```java
class Solution {
    public boolean isSubsequence(String s, String t) {
        int i = 0;
        int j = 0;
        while (i < s.length() && j < t.length()) {
            if (s.charAt(i) == t.charAt(j)) {
                i++;
            }
            j++;
        }
        return i == s.length();
    }
}
```

