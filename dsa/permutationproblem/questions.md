

### **2. Approach**

We use **backtracking with swapping**:

1. Start from an index (`start`).
2. Iterate through each position from `start` to `end`:

   * Swap the current element with the `start` element.
   * Recursively call the function for `start + 1`.
   * **Backtrack:** Swap back to restore the original order.
3. When `start == end`, print or store the permutation.

---

### **3. Java Implementation**

```java
public class Permutation {
    // Function to swap characters in a character array
    private static void swap(char[] arr, int i, int j) {
        char temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }

    // Recursive function to generate permutations
    private static void permute(char[] arr, int index) {
        if (index == arr.length - 1) {
            System.out.println(String.valueOf(arr));
            return;
        }

        for (int i = index; i < arr.length; i++) {
            // Swap to fix the current character
            swap(arr, index, i);

            // Recursive call
            permute(arr, index + 1);

            // Backtrack to restore original configuration
            swap(arr, index, i);
        }
    }

    public static void main(String[] args) {
        String str = "ABC";
        char[] arr = str.toCharArray();
        permute(arr, 0);
    }
}
```

---

### **4. Dry Run for "ABC"**

| Step             | Swap      | Current String      |
| ---------------- | --------- | ------------------- |
| Start at index 0 | Swap(0,0) | `ABC`               |
| index 1          | Swap(1,1) | `ABC` → print `ABC` |
| Backtrack        | Swap(1,2) | `ACB` → print `ACB` |
| Backtrack        | Swap(0,1) | `BAC`               |
| index 1          | Swap(1,1) | `BAC` → print `BAC` |
| Backtrack        | Swap(1,2) | `BCA` → print `BCA` |
| Backtrack        | Swap(0,2) | `CBA`               |
| index 1          | Swap(1,1) | `CBA` → print `CBA` |
| Backtrack        | Swap(1,2) | `CAB` → print `CAB` |

---

### **5. Complexity**

* **Time Complexity:**
  `O(n! * n)`
  There are `n!` permutations, and printing each takes `O(n)`.
* **Space Complexity:**
  `O(n)` recursion depth for the call stack.

---



```mermaid
graph TD
    A0["permute(ABC, 0)"]
    A1["swap(0,0) -> permute(ABC,1)"]
    A2["swap(1,1) -> permute(ABC,2) -> print(ABC)"]
    A3["swap(1,2) -> permute(ACB,2) -> print(ACB)"]
    B1["swap(0,1) -> permute(BAC,1)"]
    B2["swap(1,1) -> permute(BAC,2) -> print(BAC)"]
    B3["swap(1,2) -> permute(BCA,2) -> print(BCA)"]
    C1["swap(0,2) -> permute(CBA,1)"]
    C2["swap(1,1) -> permute(CBA,2) -> print(CBA)"]
    C3["swap(1,2) -> permute(CAB,2) -> print(CAB)"]

    A0 --> A1 --> A2
    A1 --> A3
    A0 --> B1 --> B2
    B1 --> B3
    A0 --> C1 --> C2
    C1 --> C3
