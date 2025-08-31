Given an integer array nums, return all unique triplets [a, b, c] such that:

Got it ✅ In short, duplicates are avoided by:

1. **For `i`** → skip if `nums[i] == nums[i-1]`.

   ```java
   if (i > 0 && nums[i] == nums[i - 1]) continue;
   ```

2. **For `left` and `right`** → after finding a valid triplet, move pointers and skip duplicates:

   ```java
   while (left < right && nums[left] == nums[left - 1]) left++;
   while (left < right && nums[right] == nums[right + 1]) right--;
   ```

👉 This ensures each unique triplet is added only once.





### 🔹 Approach for **3Sum Closest**

1. **Sort the array** → makes it easier to use two pointers.
2. **Fix one number (`i`)** and then use **two pointers (`left`, `right`)** to find the sum of three numbers.
3. Keep track of the **closest sum** to the target.

   * Update if `|sum - target| < |closest - target|`.
4. If `sum < target` → move `left++` (to increase sum).
   If `sum > target` → move `right--` (to decrease sum).
   If `sum == target` → return immediately (perfect match).
5. Continue until all triplets checked.
6. Return the `closest` sum.

⏱ **Time Complexity:** `O(n²)` (sorting + two-pointer loop)
📦 **Space Complexity:** `O(1)`



This is the **4Sum problem**. Here’s a short summary of the approach:

---

### ❓ Question

Given an array `nums` and an integer `target`, return **all unique quadruplets** `[a, b, c, d]` such that:

```
nums[a] + nums[b] + nums[c] + nums[d] == target
```

Each index must be distinct.

**Example 1**

```
Input: nums = [1,0,-1,0,-2,2], target = 0  
Output: [[-2,-1,1,2],[-2,0,0,2],[-1,0,0,1]]
```

**Example 2**

```
Input: nums = [2,2,2,2,2], target = 8  
Output: [[2,2,2,2]]
```

---

### 🔹 Approach

1. **Sort the array** → makes it easier to skip duplicates and use two pointers.
2. **Fix the first two numbers (`i` and `j`)** in nested loops.
3. Use **two pointers (`left` and `right`)** for the remaining two numbers.
4. Calculate the sum of the four numbers.

   * If sum < target → move `left++`
   * If sum > target → move `right--`
   * If sum == target → add quadruplet to result.
5. **Skip duplicates** for all four positions to ensure unique quadruplets.
6. Continue until all quadruplets are checked.

⏱ **Time Complexity:** `O(n³)`
📦 **Space Complexity:** `O(1)` (excluding result storage)



Got it 👍 Here’s just the **approach** (no code):

---

### **Approach for Next Permutation**

1. **Scan from right to left** and find the first index `i` such that `nums[i] < nums[i+1]`.

   * If no such index exists, the array is in descending order → reverse the whole array to get the smallest permutation.

2. **From the right**, find the first index `j` such that `nums[j] > nums[i]`.

3. **Swap** `nums[i]` and `nums[j]`.

4. **Reverse the subarray** from `i+1` to the end (to make it the smallest possible sequence after `i`).




Got it 👍 here’s only the **approach** for the **Sort Colors (Dutch National Flag problem):**

---

### **Approach**

1. Maintain three pointers:

   * `low` → boundary for placing `0`s (red).
   * `mid` → current index being checked.
   * `high` → boundary for placing `2`s (blue).

2. Traverse the array with `mid`:

   * If `nums[mid] == 0`: swap with `nums[low]`, move both `low` and `mid` forward.
   * If `nums[mid] == 1`: just move `mid` forward.
   * If `nums[mid] == 2`: swap with `nums[high]`, move `high` backward (don’t move `mid` yet).

3. Continue until `mid > high`.

4. Array will be sorted as `0`s → `1`s → `2`s (red, white, blue).


Got it 👍 Here’s the **approach for One Edit Distance**:

---

### **Approach**

1. **Check length difference**

   * If `abs(len(s) - len(t)) > 1` → return `False` (too many edits needed).

2. **Case 1: Same length (Replacement check)**

   * Traverse both strings.
   * Count mismatches.
   * If exactly **1 mismatch**, return `True`; else `False`.

3. **Case 2: Length differs by 1 (Insert/Delete check)**

   * Identify shorter and longer string.
   * Use two pointers to traverse both.
   * Allow at most **one skip** in the longer string when characters don’t match.
   * If more than one skip is needed → return `False`.

4. **Case 3: Other length difference**

   * Return `False`.