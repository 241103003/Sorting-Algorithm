Problem 1: Bubble Sort

**Problem**:  
Implement the Bubble Sort algorithm. Given an unsorted list of numbers, return the sorted list in ascending order.

**Idea**:  
Repeatedly compare adjacent elements and swap them if they are in the wrong order. Each iteration bubbles the largest unsorted element to the end.

**Hint**:  
Use nested loops. Outer loop tracks passes, inner loop does comparisons and swaps.

**Solution**:
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr
```
Problem 2: Merge Sort
Problem:
Implement Merge Sort. Given an unsorted list, sort it using a divide-and-conquer approach.

Idea:
Recursively split the list into halves, sort each half, and merge the sorted halves.

Hint:
Base case is a list of length 1. Use slicing to divide, then merge sorted results.

Solution:
```python
def merge_sort(arr):
    if len(arr) > 1:
        mid = len(arr) // 2
        L = arr[:mid]
        R = arr[mid:]

        merge_sort(L)
        merge_sort(R)

        i = j = k = 0
        while i < len(L) and j < len(R):
            if L[i] < R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1

        arr[k:] = L[i:] + R[j:]
    return arr
```
Problem 3: Quick Sort
Problem:
Sort an array using Quick Sort. Choose a pivot and partition the array such that all elements less than pivot come before it, and those greater come after.

Idea:
Recursively sort subarrays around a pivot element.

Hint:
Use list comprehensions to split around pivot. First element can be used as pivot.

Solution:
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[0]
    left = [x for x in arr[1:] if x < pivot]
    right = [x for x in arr[1:] if x >= pivot]
    return quick_sort(left) + [pivot] + quick_sort(right)

```

Problem 4: Count Sort (Counting Sort)
Problem:
Given a list of non-negative integers where the maximum value is known, implement Counting Sort.

Idea:
Count occurrences of each number, then use these counts to construct the sorted list.

Hint:
Use a frequency array of size max+1. Sum counts to build sorted output.

Solution:
```python
def counting_sort(arr):
    if not arr:
        return arr
    max_val = max(arr)
    count = [0] * (max_val + 1)
    for num in arr:
        count[num] += 1
    result = []
    for num, freq in enumerate(count):
        result.extend([num] * freq)
    return result


```
