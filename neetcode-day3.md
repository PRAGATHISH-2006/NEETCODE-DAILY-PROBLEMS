# 🧩 NeetCode Daily Solutions

📅 Date: 2026-03-11  |  ✅ Problems Solved: 3  |  🏷️ Topics: Arrays, Strings

---

## 1. Append Characters to String to Make Subsequence

**Difficulty:** 🟡 Medium  |  **Topic:** Two Pointers, String

✅ **Solution (Java)**

```java
class Solution {
    public int appendCharacters(String s, String t) {
        int i = 0;
        int j = 0;
        int n = t.length();
        while (i < s.length() && j < t.length()) {
            if (s.charAt(i) == t.charAt(j)) {
                j++;
            }
            i++;
        }
        return n - j;
    }
}
```

---

## 2. Max Consecutive Ones

**Difficulty:** 🟢 Easy  |  **Topic:** Array

✅ **Solution (Java)**

```java
class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
        List<Integer> l = new ArrayList<>();
        int c = 0;
        for (int a : nums) {
            if (a == 1) c++;
            else {
                l.add(c);
                c = 0;
            }
        }
        l.add(c);
        int n = 0;
        for (int a : l) {
            if (a > n) n = a;
        }
        return n;
    }
}
```

---

## 3. Length of Last Word

**Difficulty:** 🟢 Easy  |  **Topic:** String

✅ **Solution (Java)**

```java
class Solution {
    public int lengthOfLastWord(String s) {
        s = s.trim();
        int n = s.length();
        int a = s.lastIndexOf(" ");
        return n - a - 1;
    }
}
```

