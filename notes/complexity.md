# Search & Sorting Algorithms Complexity Analysis

## 1. Bubble Sort
- **Best Case Time:** $O(n)$ — Input is already sorted.
- **Average Case Time:** $O(n^2)$ — Random array order.
- **Worst Case Time:** $O(n^2)$ — Array sorted in reverse order.
- **Space Complexity:** $O(1)$ — Performs swaps in-place without extra heap allocation.
- **Stable:** Yes — Does not swap equal elements.
- **In-Place:** Yes — Modifies array directly in continuous memory.
- **Summary:** Simple adjacent swapping algorithm with quadratic average complexity.

---

## 2. Insertion Sort
- **Best Case Time:** $O(n)$ — Input is already sorted (only $n-1$ comparisons).
- **Average Case Time:** $O(n^2)$ — Elements randomly ordered.
- **Worst Case Time:** $O(n^2)$ — Array sorted in reverse order.
- **Space Complexity:** $O(1)$ — Auxiliary space is constant.
- **Stable:** Yes — Preserves relative order during shifting.
- **In-Place:** Yes — Shifts elements within the original array array boundary.
- **Summary:** Efficient for small dataset sizes and nearly sorted inputs.

---

## 3. Selection Sort
- **Best Case Time:** $O(n^2)$ — Requires finding minimum across remaining array regardless of order.
- **Average Case Time:** $O(n^2)$ — Random order array.
- **Worst Case Time:** $O(n^2)$ — Reverse order array.
- **Space Complexity:** $O(1)$ — Only stores minimum value index.
- **Stable:** No — Swapping non-adjacent elements can disrupt relative order.
- **In-Place:** Yes — Swaps elements in original memory space.
- **Summary:** Minimizes memory write swaps ($O(n)$ swaps total) but always takes quadratic time.

---

## 4. Merge Sort
- **Best Case Time:** $O(n \log n)$ — Recursively divides and merges regardless of initial order.
- **Average Case Time:** $O(n \log n)$ — Arbitrary element order.
- **Worst Case Time:** $O(n \log n)$ — Reverse order array.
- **Space Complexity:** $O(n)$ auxiliary array space + $O(\log n)$ recursion stack.
- **Stable:** Yes — Merge step prioritizes left subarray elements when equal.
- **In-Place:** No — Requires auxiliary arrays for combining merged halves.
- **Summary:** Guaranteed $O(n \log n)$ divide-and-conquer sorting at the cost of $O(n)$ auxiliary space.

---

## 5. Quick Sort
- **Best Case Time:** $O(n \log n)$ — Pivot continually splits array into equal halves.
- **Average Case Time:** $O(n \log n)$ — Balanced partitions across arbitrary order array.
- **Worst Case Time:** $O(n^2)$ — Array already sorted/reverse sorted with naive pivot choice.
- **Space Complexity:** $O(\log n)$ average call stack memory ($O(n)$ worst-case recursion stack).
- **Stable:** No — Long distance pivot swaps ruin relative element order.
- **In-Place:** Yes — Partitions elements within existing array bounds.
- **Asymptotic Notations:**
  - $O(n^2)$ (Upper bound / Worst case)
  - $\Omega(n \log n)$ (Lower bound / Best case)
  - $\Theta(n \log n)$ (Tight bound for average case)
- **Summary:** Fast in-place algorithm utilizing partition strategy with optimal cache locality.

---

## 6. Linear Search
- **Best Case Time:** $O(1)$ — Target element found at the first position index.
- **Average Case Time:** $O(n)$ — Target element located halfway or scattered randomly.
- **Worst Case Time:** $O(n)$ — Target element at final position or absent from array.
- **Space Complexity:** $O(1)$ — Memory usage does not depend on array size.
- **Stable:** N/A (Searching algorithm).
- **In-Place:** Yes — Reads array directly without extra dynamic allocations.
- **Summary:** Sequentially checks each array element from start to finish.

---

## 7. Binary Search
- **Best Case Time:** $O(1)$ — Target element matches mid-point element on first check.
- **Average Case Time:** $O(\log n)$ — Halves search space on each iteration step.
- **Worst Case Time:** $O(\log n)$ — Search space reduced down to single element or absent.
- **Space Complexity:** $O(1)$ iterative ($O(\log n)$ recursive call stack depth).
- **Stable:** N/A (Searching algorithm).
- **In-Place:** Yes — Search range indices calculated directly on pre-sorted array.
- **Summary:** Extremely fast search on sorted arrays by repeatedly halving search intervals.
