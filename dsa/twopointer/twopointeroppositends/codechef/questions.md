Perfect 👍
You want me to write **problem statements + approaches** for these CodeChef-style problems. I’ll give you a **short but clear problem statement** (in CodeChef style) and then the **approach**. Since CodeChef problems often vary in difficulty, I’ll keep the approach from **two-pointers / array / subarray / hashing** perspective.

---

# ✅ CodeChef Problems (with Problem + Approach)

### 1. **Count Pairs**

**Problem:** Given an array of integers and a number `K`, count the number of pairs `(i, j)` such that `A[i] + A[j] = K`.
**Approach:**

* Sort the array.
* Use **two pointers**: left at start, right at end.
* If `A[left] + A[right] == K` → count++, move both pointers.
* If sum < K → move left++.
* If sum > K → move right--.
* Complexity: **O(N log N)**.

---

### 2. **Special Substring**

**Problem:** Find the longest substring where all characters are the same.
**Approach:**

* Traverse string with two pointers.
* Count streak length of identical characters.
* Keep maximum length.
* Complexity: **O(N)**.

---

### 3. **Remove Duplicates**

**Problem:** Given a sorted array, remove duplicates in-place and return new length.
**Approach:**

* Two pointer method: one for unique index, other for scanning.
* Only copy elements when different from last unique.
* Complexity: **O(N)**.

---

### 4. **Maximum Common Elements**

**Problem:** Given two arrays, find the maximum number of common elements (intersection).
**Approach:**

* Sort both arrays.
* Use two pointers to scan simultaneously.
* Count matches.
* Complexity: **O(N log N + M log M)**.

---

### 5. **Difference Pairs**

**Problem:** Count pairs `(i, j)` such that `|A[i] - A[j]| = K`.
**Approach:**

* Sort array.
* Use two pointers: check difference.
* If difference == K → count++.
* If smaller → move right.
* If bigger → move left.
* Complexity: **O(N log N)**.

---

### 6. **The Great Run**

**Problem:** Given an array, find maximum sum of any subarray of length `K`.
**Approach:**

* Sliding window of size `K`.
* Keep current sum, update max.
* Complexity: **O(N)**.

---

### 7. **Sort Array by Parity**

**Problem:** Rearrange array so that even numbers come before odd numbers.
**Approach:**

* Two pointers: left (even side), right (odd side).
* Swap when left is odd and right is even.
* Complexity: **O(N)**.

---

### 8. **Largest Common Element in Two Arrays**

**Problem:** Find the largest element that appears in both arrays.
**Approach:**

* Sort both arrays.
* Use two pointers from end (largest side).
* If equal → return.
* Else move pointer of larger number.
* Complexity: **O(N log N)**.

---

### 9. **Array Pair Sum Divisibility**

**Problem:** Check if array elements can be paired so that sum of each pair is divisible by K.
**Approach:**

* Compute remainder counts.
* For each remainder `r`, check if `count[r] == count[K-r]`.
* Handle special cases `r=0` and `K/2`.
* Complexity: **O(N)**.

---

### 10. **Equalizing by Division**

**Problem:** Make all elements equal by dividing them by 2 any number of times.
**Approach:**

* For each number, simulate divisions until `1`.
* Track frequency of each result.
* If any frequency == n → possible.
* Complexity: **O(N log(maxA))**.

---

### 11. **Minimum Moves**

**Problem:** Find minimum moves to make all array elements equal, where each move reduces a number by 1.
**Approach:**

* Minimum moves = sum(A\[i] - min(A)).
* Complexity: **O(N)**.

---

### 12. **Chef and Two Strings**

**Problem:** Given two strings with '?' as wildcard, compute minimum and maximum Hamming distance.
**Approach:**

* Traverse characters:

  * If equal or both '?', min unchanged.
  * If mismatch with '?', max++.
  * Else both different, min++ and max++.
* Complexity: **O(N)**.

---

### 13. **Chef and Subarray**

**Problem:** Find subarray with maximum sum (Kadane’s).
**Approach:**

* Kadane’s algorithm: keep running sum and max.
* Complexity: **O(N)**.

---

### 14. **Subarray XOR**

**Problem:** Count number of subarrays whose XOR is `K`.
**Approach:**

* Prefix XOR + hashmap of frequencies.
* For each prefix XOR, check `(prefixXor ^ K)` existence.
* Complexity: **O(N)**.

---

### 15. **Chef and Memory Limit**

**Problem:** Count distinct elements in every subarray of length `K`.
**Approach:**

* Sliding window + hashmap to count frequencies.
* Maintain distinct count dynamically.
* Complexity: **O(N)**.

---

### 16. **Chef and Wedding Arrangements**

**Problem:** Partition guests into minimum groups so no conflict appears (conflict if same person appears in group).
**Approach:**

* Use hashmap to track last occurrence.
* Whenever repeat appears → start new group.
* Complexity: **O(N)**.

---

### 17. **Largest K Subsequence**

**Problem:** Find lexicographically largest subsequence of length K.
**Approach:**

* Greedy with monotonic stack.
* Remove smaller elements if future bigger available.
* Complexity: **O(N)**.

---

### 18. **Zero Array Transformation**

**Problem:** Transform array into all zeros using given operations.
**Approach:**

* Often solvable with prefix sum / difference array trick.
* Keep track of balance after each operation.
* Complexity: **O(N)**.

---

### 19. **Distinct Pairs**

**Problem:** Count number of distinct pairs `(a, b)` where `a ∈ A`, `b ∈ B`.
**Approach:**

* Take distinct sets of A and B.
* Answer = |A| × |B|.
* Complexity: **O(N + M)**.

---

### 20. **Mix the Array**

**Problem:** Given two arrays, merge them into one sorted array with no duplicates.
**Approach:**

* Sort both arrays.
* Two pointers merge.
* Skip duplicates.
* Complexity: **O(N log N + M log M)**.

---

⚡ That covers **20 CodeChef problems with problem + approach** in concise format.

Would you like me to **expand each one into full detailed explanation with dry run example** (like I did earlier for LeetCode ones) so you can use them for DSA practice notes?
