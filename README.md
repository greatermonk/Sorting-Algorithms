# Sorting-Algorithms
An Overiew on different types of Sorting Algorithms, thier complexity, usages, visualizations
In this session, we will be testing and visualizing various types of sorting algorithms to test which algorithm is suited for which task, and also analyze the complexity.

1)Selection Sort
2)Merge Sort
3)Bubble Sort
4)Quick Sort

A) Selection sort:

*Selection sort works by finding the smallest element in the list and moving it to the front of the list. This process is repeated until the entire list is sorted. Selection sort is more efficient than bubble sort for large data sets, but it is still not as efficient as some other sorting algorithms.

SELECTION SORT COMPLEXITY

*Best Case Time Complexity: O(n^2):- *

The best case time complexity of selection sort occurs when the array is already sorted. In this case, the algorithm still needs to scan the entire array for each iteration to find the minimum element, leading to a time complexity of O(n^2).

*Average Case Time Complexity: O(n^2):- *

In the average case, the algorithm needs to perform n-1 iterations, and for each iteration, it needs to scan the remaining unsorted part of the array to find the minimum element. The total number of comparisons required is (n-1) + (n-2) + ... + 2 + 1 = n(n-1)/2, which is O(n^2).

Worst Case Time Complexity: O(n^2):-

The worst case time complexity of selection sort is also O(n^2), which occurs when the array is in reverse order or in a completely unsorted state.

In all cases, the time complexity of selection sort is O(n^2), making it inefficient for large datasets. However, it has the advantage of being an in-place sorting algorithm, meaning it requires only a constant amount of additional memory space, and it is useful for educational purposes due to its simplicity.

CONCLUSION:-
It's important to note that while selection sort has its applications, it is generally not recommended for sorting large data sets due to its inefficient time complexity compared to more advanced sorting algorithms like merge sort, quicksort, or other O(n log n) algorithms. However, its simplicity and in-place nature can make it a viable choice in certain scenarios, particularly when dealing with small data sets or when there are specific memory or learning constraints.





B) MERGE SORT
Merge sort is one of the most efficient sorting algorithms. It works on the principle of Divide and Conquer based on the idea of breaking down a list into several sub-lists until each sublist consists of a single element and merging those sublists in a manner that results into a sorted list.

Merge Sort Complexity:-
Time Complexity: O(N log(N)), Merge Sort is a recursive algorithm and time complexity can be expressed as following recurrence relation.

T(n) = 2T(n/2) + θ(n)\

The above recurrence can be solved either using the Recurrence Tree method or the Master method. It falls in case II of the Master Method and the solution of the recurrence is θ(Nlog(N)). The time complexity of Merge Sort isθ(Nlog(N)) in all 3 cases (worst, average, and best) as merge sort always divides the array into two halves and takes linear time to merge two halves.

Auxiliary Space: O(N), In merge sort all elements are copied into an auxiliary array. So N auxiliary space is required for merge sort.

Applications of Merge Sort:-

1.Sorting large datasets: Merge sort is particularly well-suited for sorting large datasets due to its guaranteed worst-case time complexity of O(n log n).

2.External sorting: Merge sort is commonly used in external sorting, where the data to be sorted is too large to fit into memory.

3.Custom sorting: Merge sort can be adapted to handle different input distributions, such as partially sorted, nearly sorted, or completely

unsorted data.

Advantages Of Merge Sort:-

1)Stability: Merge sort is a stable sorting algorithm, which means it maintains the relative order of equal elements in the input array.

2)Guaranteed worst-case performance: Merge sort has a worst-case time complexity of O(N logN), which means it performs well even on large datasets.

3)Parallelizable: Merge sort is a naturally parallelizable algorithm, which means it can be easily parallelized to take advantage of multiple processors or threads.





BUBBLE SORT
Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in the wrong order. This algorithm is not suitable for large data sets as its average and worst-case time complexity is quite high.


Bubble Sort Algorithm:-
Traverse from left and compare adjacent elements and the higher one is placed at right side.

In this way, the largest element is moved to the rightmost end at first.

This process is then continued to find the second largest and place it and so on until the data is sorted.



Time Complexity: :-

The bubble sort algorithm has a time complexity of O(n^2) in the worst and average case scenarios. This is evident from the quadratic relationship between input size and iterations. As the input size increases, the number of iterations (and thus time taken) increases quadratically.


Disadvantages of Bubble Sort::-

Bubble sort has a time complexity of O(N2) which makes it very slow for large data sets.

Bubble sort is a comparison-based sorting algorithm, which means that it requires a comparison operator to determine the relative order of elements in the input data set. It can limit the efficiency of the algorithm in certain cases.


Where is the Bubble sort algorithm used?

Due to its simplicity, bubble sort is often used to introduce the concept of a sorting algorithm. In computer graphics, it is popular for its capability to detect a tiny error (like a swap of just two elements) in almost-sorted arrays and fix it with just linear complexity (2n).


Example: It is used in a polygon filling algorithm, where bounding lines are sorted by their x coordinate at a specific scan line (a line parallel to the x-axis), and with incrementing y their order changes (two elements are swapped) only at intersections of two lines.





QUICK SORT
QuickSort is a sorting algorithm based on the Divide and Conquer algorithm that picks an element as a pivot and partitions the given array around the picked pivot by placing the pivot in its correct position in the sorted array.


How does QuickSort work?:-

The key process in quickSort is a partition(). The target of partitions is to place the pivot (any element can be chosen to be a pivot) at its correct position in the sorted array and put all smaller elements to the left of the pivot, and all greater elements to the right of the pivot.

Partition is done recursively on each side of the pivot after the pivot is placed in its correct position and this finally sorts the array.



Algorithm:-
Choose Pivot: Select a pivot element from the array. There are various strategies for choosing the pivot, such as selecting the first, last, middle, or a random element.

Partitioning: Rearrange the elements of the array so that all elements less than the pivot come before it, and all elements greater than the pivot come after it. After this partitioning, the pivot is in its final sorted position.

Recursion: Recursively apply the above steps to the sub-arrays formed by partitioning until the base case is reached (typically when a sub-array has fewer than two elements).

Combine: No explicit combining step is needed, as the sorting is done in place through the partitioning process.



Complexity Analysis Of Quick Sort:-
Time Complexity:-

In the average case, Quick Sort has a time complexity of O(n log n). This is because the partitioning step divides the array into roughly equal halves, and each partitioning step takes linear time.


Space Complexity:-

Quick Sort has a space complexity of O(log n) in the best and average cases. This is because the algorithm typically uses recursion to sort sub-arrays. The maximum depth of the recursion tree is log n, where n is the number of elements in the array.






