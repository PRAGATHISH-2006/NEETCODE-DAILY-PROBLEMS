# 🧩 NeetCode Daily Solutions

**Date:** 2026-03-09  
**Problems Solved:** 3  
**Topics:** Strings, Arrays

---

## 1. Score of a String
**Difficulty:** Easy  
**Topic:** String  

### 💡 Approach
Iterate through adjacent characters and sum up the absolute differences of their ASCII values.

### ✅ Solution (Java)
```java
class Solution {
    public int scoreOfString(String s) {
        int sum = 0;
        char[] a = s.toCharArray();
        for (int i = 1; i < a.length; i++) {
            sum += Math.abs(a[i] - a[i - 1]);
        }
        return sum;
    }
}
```

### 📊 Complexity
- **Time:** O(n)
- **Space:** O(n) — due to `toCharArray()`

---

## 2. Concatenation of Array
**Difficulty:** Easy  
**Topic:** Array  

### 💡 Approach
Create a new array of double the size and fill it by iterating over the original array twice using a nested loop.

### ✅ Solution (Java)
```java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int[] a = new int[nums.length * 2];
        int ind = 0;
        for (int i = 0; i < 2; i++) {
            for (int b : nums) {
                a[ind] += b;
                ind++;
            }
        }
        return a;
    }
}
```

### 📊 Complexity
- **Time:** O(n)
- **Space:** O(n)

---

## 3. Contains Duplicate
**Difficulty:** Easy  
**Topic:** Array, Sorting  

### 💡 Approach
Sort the array first, then check adjacent elements — if any two are equal, a duplicate exists.

### ✅ Solution (Java)
```java
class Solution {
    public boolean hasDuplicate(int[] nums) {
        Arrays.sort(nums);
        for (int i = 1; i < nums.length; i++) {
            if (nums[i] == nums[i - 1]) return true;
        }
        return false;
    }
}
```

### 📊 Complexity
- **Time:** O(n log n) — due to sorting
- **Space:** O(1)


