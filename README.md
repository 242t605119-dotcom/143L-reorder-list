# LeetCode 143 – Reorder List

## Problem

Given the head of a singly linked list, reorder the list in the following pattern:

```text
L0 → L1 → L2 → ... → Ln-1 → Ln
```

into:

```text
L0 → Ln → L1 → Ln-1 → L2 → Ln-2 → ...
```

The nodes themselves must be rearranged without changing their values.

## Example 1

**Input:**

```text
head = [1,2,3,4]
```

**Output:**

```text
[1,4,2,3]
```

## Example 2

**Input:**

```text
head = [1,2,3,4,5]
```

**Output:**

```text
[1,5,2,4,3]
```

## Approach

The list can be reordered using three main steps:

1. **Find the middle** of the linked list using slow and fast pointers.
2. **Reverse the second half** of the list.
3. **Merge the two halves alternately**.

For example:

```text
1 → 2 → 3 → 4 → 5
```

First split it into:

```text
1 → 2 → 3
4 → 5
```

Reverse the second half:

```text
5 → 4
```

Then merge them alternately:

```text
1 → 5 → 2 → 4 → 3
```

## Algorithm

1. Use slow and fast pointers to find the middle of the list.
2. Split the linked list into two halves.
3. Reverse the second half.
4. Set two pointers at the beginning of both halves.
5. Take one node from the first half.
6. Take one node from the reversed second half.
7. Continue alternating until all nodes are merged.
8. The resulting list is the reordered list.

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(1)`

The list is traversed a constant number of times and no additional list or array is required.

## LeetCode Details

* **Problem Number:** 143
* **Problem Name:** Reorder List
* **Difficulty:** Medium
* **Language:** Python 3
* **File:** `solution.py`

## Topics

* Linked List
* Two Pointers
* Stack
* Recursion

## Key Learning

This problem combines several important linked-list techniques:

* Finding the middle using **two pointers**
* Reversing a linked list
* Merging two linked lists

Understanding these operations makes many more advanced linked-list problems easier to solve.

## Repository Structure

```text
leetcode-143-reorder-list/
│
├── solution.py
└── README.md
```

## Author

T.Nandhini
