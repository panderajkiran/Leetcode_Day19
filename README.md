# Leetcode_Day19
# Day 19 — LeetCode 26: Remove Duplicates from Sorted Array

## Problem

Given a sorted integer array, remove the duplicates **in-place** so that each unique element appears only once.

Return the number of unique elements `k`.

The first `k` positions of the array should contain the unique elements in sorted order.

## Approach

Since the array is already sorted, duplicate elements appear next to each other.

I used a temporary array to store only the unique elements:

1. Store the first element in the temporary array.
2. Traverse the original array from the second element.
3. Compare the current element with the last unique element.
4. If they are different, add it to the temporary array.
5. Copy the unique elements back into the original array.
6. Return the count of unique elements.

## Example

Input:
`[0,0,1,1,1,2,2,3,3,4]`

Output:
`5`

Modified array:
`[0,1,2,3,4,...]`

## Complexity

* Time Complexity: **O(n)**
* Space Complexity: **O(n)** because of the temporary array.

## Key Learning

The sorted nature of the array makes duplicate detection much easier because equal elements are always adjacent.

This problem also introduced me to the idea of the **two-pointer technique**, which can be used to solve the same problem with **O(1) extra space**.

## Takeaway

A sorted array gives us useful information. Instead of treating every element independently, we can use the order of the data to make the solution simpler and more efficient.
