📘**Topic:SortingAlgorithms**

🧠**Overview**

Sortingalgorithmsareused toarrangeelementsinaspecificorder—typically
ascendingor descending.Efficientsortingiscrucialinoptimizingother
algorithms, suchassearchandmergeoperations.

Therearetwomaincategories:

> • **Comparison-based** **sorting** (e.g.,Bubble,Merge,Quick) •
> **Non-comparison-basedsorting**(e.g.,Counting,Radix)

Eachsortingalgorithm hasitsownperformancecharacteristicsand
idealusecases.

🔢**Basic** **Concepts**

**Whatis** **Sorting?**

Sortingistheprocessoforderingelementsofalist/arraybased onacomparison
operator (e.g., \<, \>).Ithelpsimprovedataorganizationand speedsup
searching.

**SortingProperties:**

> **Property** Stability
>
> In-place
>
> TimeComplexity

**Meaning** Equalelementsretaintheir originalorder
Usesconstantextramemory(O(1)) PerformanceinBest,Average,and Worst

cases

🧮**Step-by-Step:** **Bubble** **Sort**

BubbleSortisasimple,intuitivealgorithm
thatrepeatedlyswapsadjacentelementsif theyareinthewrongorder.

**Step1:Understandthe** **logic**

Compareadjacentpairsand"bubble"thelargestelementtotheend.

**Step2:Code** **it**

def bubble_sort(arr): n = len(arr)

> for i in range(n):
>
> for j in range(0, n-i-1): if arr\[j\] \> arr\[j+1\]:
>
> arr\[j\], arr\[j+1\] = arr\[j+1\], arr\[j\]

**Step3:Visualize**

For arr = \[4, 3, 2, 1\]

> After 1stpass: \[3, 2, 1, 4\]
>
> After 2nd pass: \[2, 1, 3, 4\]
>
> …and soon.

🚀**Efficient** **Sorts:** **Merge** **and** **Quick** **Sort**

🔹**Merge** **Sort** **–Divide** **andConquer**

> 1\. Dividethearrayintohalves. 2. Recursivelysorteachhalf. 3.
> Mergesorted halves.

def merge_sort(arr): if len(arr) \> 1:

> mid = len(arr) // 2 L = arr\[:mid\]
>
> R = arr\[mid:\]
>
> merge_sort(L) merge_sort(R)
>
> i = j = k = 0
>
> while i \< len(L) and j \< len(R): if L\[i\] \< R\[j\]:
>
> arr\[k\] = L\[i\]; i += 1
>
> else:
>
> arr\[k\] = R\[j\]; j += 1
>
> k += 1
>
> arr\[k:\] = L\[i:\] + R\[j:\]

🔹**Quick** **Sort** **–Pivot** **andPartition**

def quick_sort(arr): if len(arr) \<= 1:

> return arr pivot = arr\[0\]
>
> left = \[x for x in arr\[1:\] if x \< pivot\] right = \[x for x in
> arr\[1:\] if x \>= pivot\]
>
> return quick_sort(left) + \[pivot\] + quick_sort(right)

📊**Sorting** **Algorithms** **Comparison**

> **Algorithm**
>
> BubbleSort SelectionSort InsertionSort MergeSort QuickSort Heap Sort
>
> CountingSort
>
> **Time** **Complexit** **y(Avg)**

O(n²) O(n²) O(n²) O(nlogn) O(nlogn) O(nlogn)

O(n+k)

> **Space** **Stable** **In-Place**

O(1) Yes Yes O(1) No Yes O(1) Yes Yes O(n) Yes No O(logn) No Yes O(1) No
Yes

O(k) Yes No

🔍**When** **to** **Use** **What?**

> **Scenario** Smalldataset,nearlysorted Largedataset,averagecase
> Requiresguaranteed worstcase Need topreserveorder
>
> Fixed rangeintegers

**Recommended** **Algorithm** InsertionSort

QuickSort MergeSort

StableSort(e.g.,Merge)

Counting/RadixSort

🧩**Key** **Takeaways**

> • Understand sortingproperties:stability,in-place,timecomplexity. •
> KnowwhentouseBubble,Merge,Quick,or specialized algorithms. •
> Efficientsortingisfoundationaltomanyreal-world applications.
