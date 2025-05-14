📘** Topic: Sorting Algorithms** 

🧠** Overview** 

Sorting algorithms are used to arrange elements in a specific order—typically ascending or descending. Efficient sorting is crucial in optimizing other algorithms, such as search and merge operations. 

There are two main categories: 

• **Comparison-based sorting** \(e.g., Bubble, Merge, Quick\) 

• **Non-comparison-based sorting** \(e.g., Counting, Radix\) Each sorting algorithm has its own performance characteristics and ideal use cases. 



🔢** Basic Concepts** 

**What is Sorting? ** 

Sorting is the process of ordering elements of a list/array based on a comparison operator \(e.g., <, >\). It helps improve data organization and speeds up searching. 

**Sorting Properties:** 

**Property** 

**Meaning** 

Stability 

Equal elements retain their original order In-place 

Uses constant extra memory \(O\(1\)\) Performance in Best, Average, and Worst Time Complexity cases 



🧮** Step-by-Step: Bubble Sort** Bubble Sort is a simple, intuitive algorithm that repeatedly swaps adjacent elements if they are in the wrong order. 

**Step 1: Understand the logic** Compare adjacent pairs and "bubble" the largest element to the end. 

**Step 2: Code it** 

def bubble\_sort\(arr\): 

n = len\(arr\) 

for i in range\(n\): 

for j in range\(0, n-i-1\): if arr\[j\] > arr\[j\+1\]: 

arr\[j\], arr\[j\+1\] = arr\[j\+1\], arr\[j\] 





**Step 3: Visualize** 

For arr = \[4, 3, 2, 1\] 

After 1st pass: \[3, 2, 1, 4\] 

After 2nd pass: \[2, 1, 3, 4\] 

…and so on. 



🚀** Efficient Sorts: Merge and Quick Sort** 

🔹** Merge Sort – Divide and Conquer** 1. Divide the array into halves. 

2. Recursively sort each half. 

3. Merge sorted halves. 

def merge\_sort\(arr\): 

if len\(arr\) > 1: 

mid = len\(arr\) // 2 

L = arr\[:mid\] 

R = arr\[mid:\] 



merge\_sort\(L\) merge\_sort\(R\) 



i = j = k = 0 

while i < len\(L\) and j < len\(R\): if L\[i\] < R\[j\]: 

arr\[k\] = L\[i\]; 

i \+= 1 

else: 

arr\[k\] = R\[j\]; 

j \+= 1 

k \+= 1 



arr\[k:\] = L\[i:\] \+ R\[j:\] 





🔹** Quick Sort – Pivot and Partition** def quick\_sort\(arr\): 

if len\(arr\) <= 1: 

return arr 

pivot = arr\[0\] 

left = \[x for x in arr\[1:\] if x < pivot\] 

right = \[x for x in arr\[1:\] if x >= pivot\] 

return quick\_sort\(left\) \+ \[pivot\] \+ quick\_sort\(right\) 





📊** Sorting Algorithms Comparison** **Time **

**Algorithm** 

**Complexit**

**Space** **Stable** 

**In-Place** 

**y \(Avg\)** 

Bubble Sort 

O\(n²\) 

O\(1\) 

Yes 

Yes 

Selection Sort 

O\(n²\) 

O\(1\) 

No 

Yes 

Insertion Sort 

O\(n²\) 

O\(1\) 

Yes 

Yes 

Merge Sort 

O\(n log n\) 

O\(n\) 

Yes 

No 

Quick Sort 

O\(n log n\) 

O\(log n\) No 

Yes 

Heap Sort 

O\(n log n\) 

O\(1\) 

No 

Yes 

Counting Sort 

O\(n \+ k\) 

O\(k\) 

Yes 

No 



🔍** When to Use What? ** 

**Scenario** 

**Recommended Algorithm** 

Small dataset, nearly sorted Insertion Sort 

Large dataset, average case Quick Sort 

Requires guaranteed worst case Merge Sort 

Need to preserve order 

Stable Sort \(e.g., Merge\) Fixed range integers 

Counting / Radix Sort 



🧩** Key Takeaways** 

• Understand sorting properties: stability, in-place, time complexity. 

• Know when to use Bubble, Merge, Quick, or specialized algorithms. 

• Efficient sorting is foundational to many real-world applications. 





# Document Outline

+ 📘 Topic: Sorting Algorithms 
+ 🧠 Overview 
+ 🔢 Basic Concepts  
	+ What is Sorting?  
	+ Sorting Properties: 

+ 🧮 Step-by-Step: Bubble Sort  
	+ Step 1: Understand the logic 
	+ Step 2: Code it 
	+ Step 3: Visualize 

+ 🚀 Efficient Sorts: Merge and Quick Sort  
	+ 🔹 Merge Sort – Divide and Conquer 
	+ 🔹 Quick Sort – Pivot and Partition 

+ 📊 Sorting Algorithms Comparison 
+ 🔍 When to Use What?  
+ 🧩 Key Takeaways



