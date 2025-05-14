## Snippet 1: What is Sorting?

Sorting is the process of arranging data in a specific order (usually ascending or descending).

```python
arr = [5, 3, 8, 1]
arr.sort()  # Built-in sort
print(arr)  # Output: [1, 3, 5, 8]
```
Snippet 2: Bubble Sort (In-place, Stable)
Compares adjacent elements and swaps them if out of order.
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
```
Snippet 3: Merge Sort (Stable, Not In-place)
Divide and conquer approach to sort by merging sorted halves.
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
```

Snippet 4: Quick Sort (In-place, Not Stable)
Picks a pivot and partitions elements around it.
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[0]
    left = [x for x in arr[1:] if x < pivot]
    right = [x for x in arr[1:] if x >= pivot]
    return quick_sort(left) + [pivot] + quick_sort(right)
```
Snippet 5: Counting Sort (Non-comparison, Stable)
Efficient for integers within a known range.
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
