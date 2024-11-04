# Problem: Find Minimum and Maximum in an Array

### Problem Statement
Given an array `arr`. Your task is to find the minimum and maximum elements in the array.

- **Input**: An array of integers.
- **Output**: An array that contains two elements, where the first element is the minimum and the second is the maximum of the array.

**Example**:
- **Input**: `[3, 2, 1, 56, 10000, 167]`
- **Output**: `[1, 10000]`

### Approach
1. Initialize `min_val` and `max_val` to the first element of the array.
2. Traverse through each element in the array:
   - If the element is less than `min_val`, update `min_val`.
   - If the element is greater than `max_val`, update `max_val`.
3. Return `[min_val, max_val]` as the result.

### Solution Code
```python
class Solution:
    def get_min_max(self, arr):
        # Initialize min and max
        min_val = arr[0]
        max_val = arr[0]
        
        # Traverse through the array to find min and max
        for num in arr:
            if num < min_val:
                min_val = num
            elif num > max_val:
                max_val = num
        
        return min_val, max_val


Complexity Analysis
Time Complexity: O(n), where n is the number of elements in the array (we go through the array once).
Space Complexity: O(1), as we are using only a constant amount of extra space.


Test Cases
Test Case 1:
Input: [3, 2, 1, 56, 10000, 167]
Output: [1, 10000]
Test Case 2:
Input: [1, 345, 234, 21, 56789]
Output: [1, 56789]
Test Case 3:
Input: [56789]
Output: [56789, 56789] (Single element case where min and max are the same)
