Perfect 👍 You’ve listed **20 classic Two Pointers problems**. I’ll now write the **problem statement** and a **clear approach** for each.
This will give you a strong **pattern-based reference sheet**.

---

# 🔹 Two Pointers (Opposite Ends / Same Direction)

---

### 1. Container With Most Water (LeetCode 11)

**Problem:**
Given `n` non-negative integers representing heights of vertical lines on the x-axis, find two lines that together with the x-axis form a container, such that it holds the maximum water.

**Approach:**

* Use two pointers: `left = 0`, `right = n-1`.
* Compute water = `(right - left) * min(height[left], height[right])`.
* Move the pointer with the smaller height inward.
* Keep track of max area.
* Time: **O(n)**.

---

### 2. 3Sum (LeetCode 15)

**Problem:**
Given an array `nums`, find all unique triplets `(a,b,c)` such that `a+b+c=0`.

**Approach:**

* Sort array.
* Fix one number (`i`), then use two pointers (`left, right`) to find pairs that sum to `-nums[i]`.
* Skip duplicates.
* Time: **O(n²)**.

---

### 3. 3Sum Closest (LeetCode 16)

**Problem:**
Find a triplet in array `nums` whose sum is closest to target.

**Approach:**

* Sort array.
* Fix one number, use two pointers to get closest sum.
* Keep track of min `abs(sum - target)`.
* Time: **O(n²)**.

---

### 4. 4Sum (LeetCode 18)

**Problem:**
Find all unique quadruplets `(a,b,c,d)` such that `a+b+c+d=target`.

**Approach:**

* Sort array.
* Fix two numbers using nested loops.
* Use two pointers for the remaining pair.
* Skip duplicates.
* Time: **O(n³)**.

---

### 5. Remove Duplicates from Sorted Array (LeetCode 26)

**Problem:**
Given a sorted array, remove duplicates in-place and return new length.

**Approach:**

* Use slow pointer (`j`) and fast pointer (`i`).
* Only move `j` when a new unique element is found.
* Place unique at `nums[j]`.
* Time: **O(n)**.

---

### 6. Remove Element (LeetCode 27)

**Problem:**
Remove all instances of `val` in array in-place.

**Approach:**

* Use two pointers: `i` for traversal, `j` for result placement.
* If `nums[i] != val`, assign `nums[j]=nums[i]`.
* Return `j`.
* Time: **O(n)**.

---

### 7. Move Zeroes (LeetCode 283)

**Problem:**
Move all `0`s to the end while maintaining order of non-zeros.

**Approach:**

* Use two pointers: `j` (position to insert non-zero).
* Traverse `i`, whenever non-zero, swap `nums[i]` and `nums[j]`.
* Time: **O(n)**.

---

### 8. Sort Colors (LeetCode 75)

**Problem:**
Sort array of `0,1,2` in-place (Dutch National Flag problem).

**Approach:**

* Use three pointers: `low, mid, high`.
* Swap `0` to front, `2` to back.
* Keep `1` in middle.
* Time: **O(n)**.

---

### 9. Merge Sorted Array (LeetCode 88)

**Problem:**
Merge two sorted arrays into first array (in-place).

**Approach:**

* Use three pointers from end: `i = m-1`, `j = n-1`, `k = m+n-1`.
* Place larger element at `nums1[k]`.
* Time: **O(m+n)**.

---

### 10. Valid Palindrome (LeetCode 125)

**Problem:**
Check if string is palindrome ignoring non-alphanumeric and case.

**Approach:**

* Use two pointers: `left=0, right=n-1`.
* Skip non-alphanumeric.
* Compare lowercase chars.
* Time: **O(n)**.

---

### 11. Two Sum II – Input Sorted (LeetCode 167)

**Problem:**
Given sorted array, return indices of two numbers that add up to target.

**Approach:**

* Use two pointers: `left=0, right=n-1`.
* If sum > target → move right;
* If sum < target → move left.
* Time: **O(n)**.

---

### 12. Rotate Array (LeetCode 189)

**Problem:**
Rotate array `k` steps to right.

**Approach:**

* Reverse entire array.
* Reverse first `k`.
* Reverse rest.
* Time: **O(n)**.

---

### 13. Reverse Words in a String (LeetCode 151)

**Problem:**
Reverse the words order in a string.

**Approach:**

* Trim spaces, split words.
* Reverse array of words.
* Join with space.
* Two pointers for cleanup.
* Time: **O(n)**.

---

### 14. Boats to Save People (LeetCode 881)

**Problem:**
Each boat carries 2 people with weight limit. Find minimum boats.

**Approach:**

* Sort array.
* Use two pointers (`i, j`).
* If `people[i] + people[j] <= limit` → pair them.
* Else, put `j` alone.
* Time: **O(n log n)**.

---

### 15. Longest Mountain in Array (LeetCode 845)

**Problem:**
Find length of longest mountain (increasing then decreasing subarray).

**Approach:**

* Use two pointers to expand left & right from a peak.
* Track max length.
* Time: **O(n)**.

---

### 16. Trapping Rain Water (LeetCode 42)

**Problem:**
Find water trapped after rain given elevation map.

**Approach:**

* Two pointers: `left, right`.
* Track `leftMax`, `rightMax`.
* Water += min(leftMax, rightMax) - height.
* Time: **O(n)**.

---

### 17. Minimum Size Subarray Sum (LeetCode 209)

**Problem:**
Find minimal length of subarray with sum ≥ target.

**Approach:**

* Use sliding window (`left` pointer).
* Expand right until sum ≥ target.
* Shrink left to minimize.
* Time: **O(n)**.

---

### 18. Partition List (LeetCode 86)

**Problem:**
Partition linked list around value `x` (less first, then greater/equal).

**Approach:**

* Use two dummy lists: `less`, `greater`.
* Traverse, append nodes.
* Connect lists.
* Time: **O(n)**.

---

### 19. Number of Subsequences That Satisfy Given Sum (LeetCode 1498)

**Problem:**
Count subsequences where `min + max ≤ target`.

**Approach:**

* Sort array.
* Use two pointers (`i, j`).
* If `nums[i]+nums[j] ≤ target` → add `2^(j-i)` subsequences.
* Else `j--`.
* Time: **O(n log n)** (due to sorting).

---

### 20. Squares of a Sorted Array (LeetCode 977)

**Problem:**
Return squares of sorted array in non-decreasing order.

**Approach:**

* Use two pointers: `left=0, right=n-1`.
* Compare absolute values, put larger square at end of result array.
* Time: **O(n)**.

---

✅ This covers **20 problems** with **problem statements + approaches** under the **Two Pointers** pattern.

Would you like me to create the **next pattern (Sliding Window: 10–15 problems with approach)** in the same structured way?
