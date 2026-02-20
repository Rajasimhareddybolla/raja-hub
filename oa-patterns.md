# HackerRank OA - Core Pattern Review

## 1. Grid Traversal (DFS)
**Pattern:** Number of Islands
**Key Insight:** Use `ROWS, COLS = len(grid), len(grid[0])`. Mark visited with `grid[r][c] = '-1'`. Check bounds carefully.
**Time:** $O(M \times N)$ | **Space:** $O(M \times N)$ (stack)

## 2. Hash Maps
**Pattern:** Group Anagrams
**Key Insight:** Avoid custom sum-based hashes (collisions!). Use `tuple(sorted(s))` or a 26-char frequency array as the key.
**Time:** $O(N \times K)$ | **Space:** $O(N \times K)$

## 3. Sliding Window
**Pattern:** Longest Substring Without Repeating Characters
**Key Insight:** If `s[right]` is in the set, shrink `left` until the duplicate is gone. Update `max_len` at every step.
**Time:** $O(N)$ | **Space:** $O(1)$ (alphabet size)

## 4. Trees (BFS / Level Order)
**Pattern:** Binary Tree Right Side View
**Key Insight:** Use `collections.deque`. Process level-by-level with `level_size`. Capture the last node of each level.
**Time:** $O(N)$ | **Space:** $O(N)$

## 5. Monotonic Stack
**Pattern:** Daily Temperatures / Next Greater Element
**Key Insight:** Use a stack to store *indices* of elements waiting for a higher value. Pop when current element is greater.
**Time:** $O(N)$ | **Space:** $O(N)$
