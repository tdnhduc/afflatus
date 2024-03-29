# Number type of sort:
https://en.wikipedia.org/wiki/Category:Sorting_algorithms

### Simple sorts[[edit](https://en.wikipedia.org/w/index.php?title=Sorting_algorithm&action=edit&section=9 "Edit section: Simple sorts")]

Two of the simplest sorts are **insertion sort and selection sort**, both of which are efficient on small data, due to low overhead, but not efficient on large data. Insertion sort is generally faster than selection sort in practice, due to fewer comparisons and good performance on almost-sorted data, and thus is preferred in practice, but selection sort uses fewer writes, and thus is used when write performance is a limiting factor.
### Efficient sorts[[edit](https://en.wikipedia.org/w/index.php?title=Sorting_algorithm&action=edit&section=12 "Edit section: Efficient sorts")]

Practical general sorting algorithms are almost always based on an algorithm with average time complexity (and generally worst-case complexity) O(_n_  log  _n_), of which the most common are **heapsort, merge sort, and quicksort**. Each has advantages and drawbacks, with the most significant being that simple implementation of merge sort uses O(_n_) additional space, and simple implementation of quicksort has O(_n_2) worst-case complexity. These problems can be solved or ameliorated at the cost of a more complex algorithm
### Bubble sort and variants[[edit](https://en.wikipedia.org/w/index.php?title=Sorting_algorithm&action=edit&section=17 "Edit section: Bubble sort and variants")]

Bubble sort, and variants such as the  [Shellsort](https://en.wikipedia.org/wiki/Shellsort "Shellsort")  and  [cocktail sort](https://en.wikipedia.org/wiki/Cocktail_sort "Cocktail sort"), are simple, highly inefficient sorting algorithms. They are frequently seen in introductory texts due to ease of analysis, but they are rarely used in practice.

### Distribution sorts[[edit](https://en.wikipedia.org/w/index.php?title=Sorting_algorithm&action=edit&section=21 "Edit section: Distribution sorts")]

See also:  [External sorting](https://en.wikipedia.org/wiki/External_sorting "External sorting")

_Distribution sort_  refers to any sorting algorithm where data is distributed from their input to multiple intermediate structures which are then gathered and placed on the output. For example, both  [bucket sort](https://en.wikipedia.org/wiki/Bucket_sort "Bucket sort")  and  [flashsort](https://en.wikipedia.org/wiki/Flashsort "Flashsort")  are distribution based sorting algorithms. Distribution sorting algorithms can be used on a single processor, or they can be a  [distributed algorithm](https://en.wikipedia.org/wiki/Distributed_algorithm "Distributed algorithm"), where individual subsets are separately sorted on different processors, then combined. This allows  [external sorting](https://en.wikipedia.org/wiki/External_sorting "External sorting")  of data too large to fit into a single computer's memory.

## Schwartzian transform
In [computer programming](https://en.wikipedia.org/wiki/Computer_programming "Computer programming"), the **Schwartzian transform** is a technique used to improve the efficiency of [sorting](https://en.wikipedia.org/wiki/Sorting "Sorting") a list of items. This [idiom](https://en.wikipedia.org/wiki/Programming_idiom "Programming idiom")[[1]](https://en.wikipedia.org/wiki/Schwartzian_transform#cite_note-1) is appropriate for [comparison-based sorting](https://en.wikipedia.org/wiki/Comparison_sort "Comparison sort") when the ordering is actually based on the ordering of a certain property (the _key_) of the elements, where computing that property is an intensive operation that should be performed a minimal number of times. The Schwartzian transform is notable in that it does not use named temporary arrays.

##  External sorting
**External sorting** is a class of [sorting](https://en.wikipedia.org/wiki/Sorting "Sorting")  [algorithms](https://en.wikipedia.org/wiki/Algorithm "Algorithm") that can handle massive amounts of [data](https://en.wikipedia.org/wiki/Data "Data"). External sorting is required when the data being sorted do not fit into the [main memory](https://en.wikipedia.org/wiki/Main_memory "Main memory") of a computing device (usually [RAM](https://en.wikipedia.org/wiki/RAM "RAM")) and instead they must reside in the slower [external memory](https://en.wikipedia.org/wiki/Auxiliary_memory "Auxiliary memory"), usually a [disk drive](https://en.wikipedia.org/wiki/Disk_drive "Disk drive"). Thus, external sorting algorithms are [external memory algorithms](https://en.wikipedia.org/wiki/External_memory_algorithm "External memory algorithm") and thus applicable in the [external memory](https://en.wikipedia.org/wiki/External_memory_model "External memory model")  [model of computation](https://en.wikipedia.org/wiki/Model_of_computation "Model of computation").

## K-sorted sequence
In [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"), a **nearly-sorted sequence**, also known as **roughly-sorted sequence** and as **{\displaystyle k}![k](https://wikimedia.org/api/rest_v1/media/math/render/svg/c3c9a2c7b599b37105512c5d570edc034056dd40)-sorted sequence** is a sequence which is almost ordered. By almost ordered, it is meant that no element of the sequence is very far away from where it would be if the sequence were perfectly ordered. It is still possible that no element of the sequence is at the place where it should be if the sequence were perfectly ordered.

## Partial sorting

In  [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"),  **partial sorting**  is a  [relaxed](https://en.wikipedia.org/wiki/Relaxation_(approximation) "Relaxation (approximation)")  variant of the  [sorting](https://en.wikipedia.org/wiki/Sorting_algorithm "Sorting algorithm")  problem. Total sorting is the problem of returning a list of items such that its elements all appear in order, while partial sorting is returning a list of the  _k_  smallest (or  _k_  largest) elements in order. The other elements (above the  _k_  smallest ones) may also be sorted, as in an in-place partial sort, or may be discarded, which is common in streaming partial sorts. A common practical example of partial sorting is computing the "Top 100" of some list.

In terms of indices, in a partially sorted list, for every index  _i_  from 1 to  _k,_  the  _i_-th element is in the same place as it would be in the fully sorted list: element  _i_  of the partially sorted list contains  [order statistic](https://en.wikipedia.org/wiki/Order_statistic "Order statistic")  _i_  of the input list.

## Selection algorithm
In [computer science](https://en.wikipedia.org/wiki/Computer_science "Computer science"), a **selection algorithm** is an [algorithm](https://en.wikipedia.org/wiki/Algorithm "Algorithm") for finding the _k_th smallest number in a [list](https://en.wikipedia.org/wiki/List_(abstract_data_type) "List (abstract data type)") or [array](https://en.wikipedia.org/wiki/Array_data_structure "Array data structure"); such a number is called the _k_th _[order statistic](https://en.wikipedia.org/wiki/Order_statistic "Order statistic")_. This includes the cases of finding the [minimum](https://en.wikipedia.org/wiki/Minimum "Minimum"), [maximum](https://en.wikipedia.org/wiki/Maximum "Maximum"), and [median](https://en.wikipedia.org/wiki/Median "Median") elements. There are O(_n_)-time (worst-case linear time) selection algorithms, and sublinear performance is possible for structured data; in the extreme, O(1) for an array of sorted data. Selection is a subproblem of more complex problems like the [nearest neighbor](https://en.wikipedia.org/wiki/Nearest_neighbor_problem "Nearest neighbor problem") and [shortest path](https://en.wikipedia.org/wiki/Shortest_path "Shortest path") problems. Many selection algorithms are derived by generalizing a [sorting algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm "Sorting algorithm"), and conversely some sorting algorithms can be derived as repeated application of selection.

## Random_permutation
If a computer has access to purely random numbers, it is capable of generating a "perfect shuffle", a [random permutation](https://en.wikipedia.org/wiki/Random_permutation "Random permutation") of the cards; beware that this terminology (an algorithm that perfectly randomizes the deck) differs from "a perfectly executed single shuffle", notably a perfectly interleaving [faro shuffle](https://en.wikipedia.org/wiki/Faro_shuffle "Faro shuffle"). The [Fisher–Yates shuffle](https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle "Fisher–Yates shuffle"), popularized by [Donald Knuth](https://en.wikipedia.org/wiki/Donald_Knuth "Donald Knuth"), is simple (a few lines of code) and efficient ([O](https://en.wikipedia.org/wiki/Big_O_notation "Big O notation")(_n_) on an _n_-card deck, assuming constant time for fundamental steps) algorithm for doing this. Shuffling can be seen as the opposite of [sorting](https://en.wikipedia.org/wiki/Sorting_algorithm "Sorting algorithm").

## BogoSort

In [computer science](https://en.wikipedia.org/wiki/Computer_science), **bogosort**[[1]](https://en.wikipedia.org/wiki/Bogosort#cite_note-Fun07-1)[[2]](https://en.wikipedia.org/wiki/Bogosort#cite_note-KSFS-2) (also known as **permutation sort**, **stupid sort**,[[3]](https://en.wikipedia.org/wiki/Bogosort#cite_note-3) or **slowsort**[[4]](https://en.wikipedia.org/wiki/Bogosort#cite_note-Naish86-4)) is a [sorting algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm "Sorting algorithm") based on the [generate and test](https://en.wikipedia.org/wiki/Generate_and_test "Generate and test") paradigm. The function successively generates [permutations](https://en.wikipedia.org/wiki/Permutation "Permutation") of its input until it finds one that is sorted. It is not considered useful for sorting, but may be used for educational purposes, to contrast it with more efficient algorithms.

## Bead Sort
**Bead sort**, also called **gravity sort**, is a [natural](https://en.wikipedia.org/wiki/Natural_computing "Natural computing")  [sorting algorithm](https://en.wikipedia.org/wiki/Sorting_algorithm "Sorting algorithm"), developed by [Joshua J. Arulanandham](https://en.wikipedia.org/w/index.php?title=Joshua_J._Arulanandham&action=edit&redlink=1 "Joshua J. Arulanandham (page does not exist)"), [Cristian S. Calude](https://en.wikipedia.org/wiki/Cristian_S._Calude "Cristian S. Calude") and [Michael J. Dinneen](https://en.wikipedia.org/wiki/Michael_J._Dinneen "Michael J. Dinneen") in 2002, and published in _The Bulletin of the  [European Association for Theoretical Computer Science](https://en.wikipedia.org/wiki/European_Association_for_Theoretical_Computer_Science "European Association for Theoretical Computer Science")_.[[1]](https://en.wikipedia.org/wiki/Bead_sort#cite_note-bead-sort-paper-1) Both [digital](https://en.wikipedia.org/wiki/Digital_data "Digital data") and [analog](https://en.wikipedia.org/wiki/Analog_computer "Analog computer") hardware [implementations](https://en.wikipedia.org/wiki/Implementation "Implementation") of bead sort can achieve a sorting time of _[O](https://en.wikipedia.org/wiki/Big_O_Notation "Big O Notation")_(_n_); however, the implementation of this algorithm tends to be significantly slower in [software](https://en.wikipedia.org/wiki/Software "Software") and can only be used to sort lists of [positive integers](https://en.wikipedia.org/wiki/Positive_integer "Positive integer"). Also, it would seem that even in the best case, the algorithm requires _[O](https://en.wikipedia.org/wiki/Big_O_Notation "Big O Notation")_(_n2_) space.


# Compare Sort Methods :
| Names        | Average           |  Memory |Note|
|:------------- |:-------------:| -----:|:-------------|
|    **Quick sort**   | $n\log{n}$ | $\log{n}$ ||
| **Merge Sort**| $n\log{n}$| $n$|Best-Average-Worst is the same|
| **Heap Sort** |$n\log{n}$|$1$||
|**Insertion Sort**|$n^2$|1|Worst-case when array is inverse, best case O(n)|
|**Selection Sort**|$n^2$|1||
|**Bubble Sort**|$n^2$|1|Few code|
|**Tree Sort**|$n\log{n}$|$n$|Worst-case is $n\log{n}$ when it's balanced tree|
# Code 
1. **Quick sort**
> Idea: It picks an element as a pivot and partitions the given array around the picked pivot. There are many different versions of quickSort that pick pivot in different ways.
```python
def partition(arr, low, high):
	i = low - 1 # index of smaller element
	pivot = arr[high]
	for j in range(low, high):
	if arr[j] <= pivot:
		i += 1
		arr[i],arr[j] = arr[j],arr[i]
	arr[i+1], arr[high] = arr[high], arr[i+1]
	return i+1

def quickSort(arr, low, high):
	if low < high:
		pi = partition(arr, low, high)
		quickSort(arr, low, pi - 1)
		quickSort(arr, pi + 1, high)
# example : quickSort(arr, 0, len(arr) - 1)
```
2. **Merge Sort**:
> Idea: So, in this algorithm, the array is **initially divided into two equal** halves and then they are combined in a sorted manner. We can think of it as a recursive algorithm that continuously splits the array in half until it cannot be further divided. This means that if the array becomes empty or has only one element left, the dividing will stop, i.e. it is the base case to stop the recursion. If the array has multiple elements, we split the array into halves and recursively invoke the merge sort on each of the halves. Finally, when both the halves are sorted, the merge operation is applied. Merge operation is the process of taking two smaller sorted arrays and combining them to eventually make a larger one.
```python
def merge(arr, l, m, r):
	n1 = m - l + 1
	n2 = r - m
	# Create temp arrays
	L = [0] * n1
	R = [0] * n2 
	# Copy data to temp arrays
	for i in range(n1):
		L[i] = arr[l+i]
	for j in range(0, n2):
		R[j] = arr[m + 1 + j]
	# Merge back into array
	i = 0
	j = 0
	k = l
	while i < n1 and j < n2:
		if L[i] <= R[j]:
			arr[k] = L[i]
			i += 1
		else:
			arr[k] = R[j]
			j += 1
		k += 1
	while i < n1:
		arr[k] = L[i]
		i += 1
		k += 1
	while j < n2:
		arr[k] = R[j]
		j += 1
		k += 1
def mergeSort(arr, l, r):
	if l < r:
		m = (l + (r - 1)) // 2
		mergeSort(arr, l, m)
		mergeSort(arr, m + 1, r)
		merge(arr, l, m, r)
# example : mergeSort(arr, 0, len(arr) - 1)
```
3. **Heap Sort**
```python
def heapify(arr, n, i):
	largest = i
	l = 2 * i + 1
	r = 2 * i + 2
	if l < n and arr[i] < arr[l]:
		largest = l
	if r < n and arr[largest] < arr[r]:
		largest = r
	if largest != i:
		arr[i], arr[largest] = arr[largest], arr[i]
		heapify(arr, n, largest)
def heapSort(arr):
	n = len(arr)
	for i in range(n//2 - 1, -1, -1):
		heapify(arr, n, i)
	for i in range(n - 1, 0, -1):
		arr[i], arr[0] = arr[0], arr[i]
		heapify(arr, i, 0)
# source : https://www.geeksforgeeks.org/python-program-for-heap-sort/
```
4. **Insertion Sort**:
> continue ...
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMzAyNjY3MzAsLTEzNTEzMTg1OTYsMj
YzNjk5NzcyLDE1ODgyODk4MDIsLTExNzE5NTg2OTUsLTc5Nzgy
NjM2NCwtODU5MTc3Mzg5LC0xNTMzOTc2OTg0XX0=
-->