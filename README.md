# Two Sum

## Problem
Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to the target.

You may assume that each input has exactly one solution, and you may not use the same element twice.

---

## Example

Input

nums = [2,7,11,15]
target = 9


Output

[0,1]


Explanation  
`nums[0] + nums[1] = 2 + 7 = 9`

---

## Approach

This solution uses a **brute-force approach**.

1. Traverse the array using the first loop.
2. For each element, check the remaining elements using a second loop.
3. If the sum of two elements equals the target, return their indices.

---

## Algorithm

1. Start a loop from `i = 0` to `nums.length`
2. Start another loop from `j = i + 1` to `nums.length`
3. Check if `nums[i] + nums[j] == target`
4. If true, return `[i, j]`
5. If no pair is found, return an empty array

---

## Java Implementation

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for(int i = 0 ; i < nums.length; i++){
            for(int j = i + 1 ; j < nums.length; j++){
                if(nums[i] + nums[j] == target)
                    return new int[]{i , j};
            }
        }
        return new int[0];
    }
}
Complexity Analysis

Time Complexity

O(n²)

Space Complexity

O(1)
Author

Sanjeev Sharma
