Perfect! Let’s expand each **Codeforces Two-Pointer problem** with **more detailed problem description and approach**, so it’s easier to understand and use for practice. I’ll keep them in a structured way like before.

---

# 🔹 Codeforces — Two Pointers Pattern (Expanded)

---

### 1. **279B — Books**

**Problem:**
You have `n` books in a row; each book takes `t[i]` minutes to read. You have total time `T`. You want to read a consecutive sequence of books. Find the **maximum number of books** you can read without exceeding `T`.

**Approach:**

* Use **sliding window**.
* Maintain two pointers `left` and `right`. Expand `right` adding `t[right]` to sum.
* If sum > T, move `left` forward to shrink window.
* Keep track of **max window length**.
* **Time Complexity:** O(n).

---

### 2. **580A — Kefa and First Steps**

**Problem:**
Given an array of integers, find the **length of the longest non-decreasing contiguous subarray**.

**Approach:**

* Two pointers: `start` and `end`.
* Expand `end` while `arr[end] >= arr[end-1]`.
* When it breaks, reset `start = end`.
* Keep track of max length.
* **Time Complexity:** O(n).

---

### 3. **6C — Alice, Bob and Chocolate**

**Problem:**
Alice and Bob eat chocolates from opposite ends. Each chocolate takes time equal to its weight. Determine **how many chocolates each eats**.

**Approach:**

* Two pointers: `left` and `right`.
* Maintain `sumAlice` and `sumBob`.
* Move `left` or `right` depending on who has smaller total time.
* Stop when pointers meet.
* **Time Complexity:** O(n).

---

### 4. **381A — Sereja and Dima**

**Problem:**
Two players take numbers from either end of an array. Each player wants **maximum total sum**. Determine their scores if both play optimally.

**Approach:**

* Two pointers: `left` and `right`.
* Player chooses **max(arr\[left], arr\[right])** each turn.
* Move pointer corresponding to chosen element.
* Simulate game alternately.
* **Time Complexity:** O(n).

---

### 5. **381B — Georg and Permutation**

**Problem:**
Choose a subsequence from a permutation such that **consecutive numbers differ by at least 2**. Maximize its length.

**Approach:**

* Sort array (or keep order in permutation).
* Use two pointers to scan array, select number if difference ≥2 with previous chosen.
* **Time Complexity:** O(n).

---

### 6. **1138A — Sushi for Two**

**Problem:**
Given sequence of sushi types (1 and 2), find the **longest alternating sequence**.

**Approach:**

* Count contiguous blocks of 1s and 2s.
* Two pointers scan through blocks, take min of adjacent blocks to form alternating sequence.
* **Time Complexity:** O(n).

---

### 7. **545C — Woodcutters**

**Problem:**
You can cut a tree to the left or right. No two trees can fall on each other. Maximize the number of trees that can be cut.

**Approach:**

* Two pointers simulate cutting each tree.
* Maintain previous tree position.
* If left cut possible → cut left; else if right cut → cut right; else leave tree.
* **Time Complexity:** O(n).

---

### 8. **1006C — Three Parts of the Array**

**Problem:**
Split array into three parts with equal sum. Maximize the number of ways.

**Approach:**

* Compute total sum.
* Use two pointers to find prefix and suffix matching 1/3 of total sum.
* Count middle possibilities.
* **Time Complexity:** O(n).

---

### 9. **1041B — Buying a TV Set**

**Problem:**
Fit TV of ratio `a:b` into room of size `x,y`. Find maximum possible size.

**Approach:**

* Reduce ratio `a:b` using gcd.
* Two pointers style: scale width and height proportionally until max fits in `x,y`.
* **Time Complexity:** O(1) (simple math).

---

### 10. **1029B — Creating the Contest**

**Problem:**
Arrange problems in sequence so each ≤ 2× previous. Maximize number of problems used.

**Approach:**

* Sort array.
* Use two pointers sliding window to track sequence meeting condition.
* **Time Complexity:** O(n log n).

---

### 11. **1370B — GCD Compression**

**Problem:**
Pair numbers so exactly `n-1` pairs satisfy certain property (like gcd>1).

**Approach:**

* Sort numbers.
* Use two pointers to group compatible numbers.
* **Time Complexity:** O(n log n).

---

### 12. **1324C — Frog Jumps**

**Problem:**
Frog jumps between stones with `R`s, find maximum distance it must jump.

**Approach:**

* Scan string with two pointers between consecutive `R`s.
* Keep max gap.
* **Time Complexity:** O(n).

---

### 13. **676C — Vasya and String**

**Problem:**
Max length substring where ≤k characters can be changed to make string all same character.

**Approach:**

* Sliding window: expand right, count changes needed.
* If changes > k → move left.
* Keep max window length.
* **Time Complexity:** O(n).

---

### 14. **615A — Bulbs**

**Problem:**
Check if all bulbs can be turned on using given switches.

**Approach:**

* Two pointers or array prefix sum to simulate effect of switch.
* Verify final state.
* **Time Complexity:** O(n).

---

### 15. **1256C — Platforms Jumping**

**Problem:**
Jump on platforms with max jump distance `d`. Count number of ways or minimum jumps.

**Approach:**

* Sort platforms.
* Two pointers to find next reachable platform within `d`.
* **Time Complexity:** O(n).

---

### 16. **1335C — Two Teams Composing**

**Problem:**
Divide numbers into balanced teams.

**Approach:**

* Count frequency of each number.
* Use two pointers to match small and large frequencies to maximize teams.
* **Time Complexity:** O(n log n).

---

### 17. **1201B — Zero Array**

**Problem:**
Reduce array to all zeros using allowed operations.

**Approach:**

* Two pointers: sort array, adjust difference between left/right to zero.
* **Time Complexity:** O(n log n).

---

### 18. **1462B — Last Year’s Substring**

**Problem:**
Check if string “2020” can be formed using prefix+suffix.

**Approach:**

* Two pointers from start/end to check first `k` and last `4-k` chars.
* **Time Complexity:** O(1).

---

### 19. **1481B — New Colony**

**Problem:**
Simulate pouring sand piles with `k` moves.

**Approach:**

* Two pointers scan left to right.
* Track remaining moves and distribute as allowed.
* **Time Complexity:** O(n).

---

### 20. **1409A — Yet Another Two Integers Problem**

**Problem:**
Min moves to make two integers equal using steps of size ≤10.

**Approach:**

* Difference = |a-b|.
* Number of moves = ceil(difference / 10).
* Two pointers style not needed, simple math.
* **Time Complexity:** O(1).

---

✅ Now all **20 Codeforces Two Pointer problems** have **detailed problem descriptions and approaches**.

---

If you want, I can **also make a master table with all 60 problems** (LeetCode + CodeChef + Codeforces) **with problem + approach in one sheet**, so it’s ready for study and practice.

Do you want me to do that next?
