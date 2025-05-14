## Sorting Algorithms – Interview Q&A

### Question 1  
**Q: What is the difference between comparison-based and non-comparison-based sorting algorithms?**  
**A:**  
Comparison-based algorithms (e.g., Quick Sort, Merge Sort, Bubble Sort) determine the order based on pairwise comparisons. Non-comparison-based algorithms (e.g., Counting Sort, Radix Sort) use the value of elements directly, making them faster for certain data types like integers within a fixed range.

---

### Question 2  
**Q: Why is Quick Sort considered efficient on average but not in the worst case?**  
**A:**  
Quick Sort has an average time complexity of O(n log n), but in the worst case (e.g., when the pivot always picks the largest or smallest element), it degrades to O(n²). However, with good pivot selection (like randomized or median-of-three), the worst case is rare.

---

### Question 3  
**Q: What makes Merge Sort stable, and why is that important?**  
**A:**  
Merge Sort preserves the relative order of equal elements because it never swaps them arbitrarily. Stability is important when sorting records with multiple fields — it ensures that sorting by one field doesn’t disrupt prior orderings by another.

---

### Question 4  
**Q: When is Counting Sort preferable over comparison-based algorithms?**  
**A:**  
Counting Sort is ideal when input consists of integers within a small, known range. It achieves linear time complexity, O(n + k), but requires extra space and doesn’t work well for large ranges or floating-point values.

---

### Question 5  
**Q: What is an in-place sorting algorithm? Provide examples.**  
**A:**  
An in-place algorithm uses a constant amount of extra memory (O(1)). Examples include Bubble Sort, Selection Sort, and Quick Sort (depending on implementation). In-place sorting is memory-efficient, which can be crucial for large datasets.
