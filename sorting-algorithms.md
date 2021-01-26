
  ## **What is an Algorithm?**
  Simply put, an algorithm is a process. And like any process, an algorithm contains a set of steps you take in order to achieve a specific goal.

  Here are some algorithims we encounter in our daily lives!
<details>
<summary>Making Toast</summary>

1. Get a slice of bread
2. Place the slice of bread in the toaster
3. Turn the toaster on
4. Wait a few minutes
5. Take the toast out of the toaster
6. Place the toast on a plate 
</details>

<details>
<summary>Brushing your teeth</summary>

1. Get you tooth brush
2. Get you tooth paste
3. Open the tooth paste
4. Push on the tooth paste until it gets onto the brush
5. Brush teeth back and forth for two minuets
6. Rinse you mouth
</details>

<br>

- There may be several different algorithms that can sort or find a value in a data set, and some of these may execute more quickly than others. Studying algorithms gives us the knowledge we need to find the best way to approach a problem.

- No matter its use, an algorithm is simply a set of instructions that tells a computer how to solve a problem.

- A search algorithm retrieves information stored within a data structure.

- A sorting algorithm puts elements in a list in a certain order. This might sound simple, but when your data set has thousands, or even millions, of different items, it gets much more difficult.

- Algorithms are evaluated based on their computational complexity, or the amount of resources it takes to run them. Those resources include:

    - **Time**: The maximum amount of time it would take the algorithm to solve a problem.

    - **Space**: The maximum amount of computer memory, or RAM, the algorithm needs to run.

- Space: The maximum amount of computer memory, or RAM, the algorithm needs to run.


## Introduction to Sorting
  
- **Comparison sorts** (comparing one value to another) versus **distribution sorts** (groupings items by a characteristic).
- **Stability**: If a data set remains in place when it’s sorted multiple times.


<details>
<summary>Basic Sorting Algorithms</summary>
  These sorting methods are slow, inefficient, rarely used, but simpler to learn, more intuitive, and a good starting point


Name | Description | BigO Time | Big0 Space | Stability | Use Cases
--- | --- | --- | --- | --- | ---
Bubble | Because items have to 'bubble' to their correct position in the list.......1. Start at the beginning of the array. 2. Compare the current item to the next item. 3. If the current item is greater, you swap places; if the current item is smaller, that’s great and keep it in place. 4.Move onto the next item and keep comparing. 5.Keep going through the array until no swaps happen | 0(N^2) - not good for large datasets |  0(1) - no new arrays created regardless of data size | Stable: items remain sorted as we loop through the array. | Rarely used in real life due to its quadratic worst case run time.  A good sorting algorithm for beginners
Insertion | “Insertion” because you take each item and insert it into its correct position.  Think of how someone would sort a handful of playing cards......Start with first item and think of it as being in its own sorted section. Take its next door neighbor and compare it. Move it to the right place in the sorted section of the array by comparing it one at a time with the items in the sorted array. | O(N^2) - you have to traverse the array repeatedly to insert the current value, inefficient for large data. | O(1) - no new arrays created regardless of input size. | Stable: items remain sorted while we loop through the array. | Used IRL for small datasets.
</details>

<details>
<summary>Divide-and-Conquer Sorting Algorithms</summary>
  
Name | Description | BigO Time | Big0 Space | Stability | Use Cases
--- | --- | --- | --- | --- | ---
Merge | “Merge” because you split up the array into small and sorted parts, then merge the small pieces together into sorted smaller arrays until you have one big array again.  This is usually split up into two functions, a recursive MergeSort that splits the array recursively and a Merge helper function that joins the pieces back together.....1: Merge Sort: Take the array and split it in half over and over again until you have one-item long (sorted) arrays.  2: Merge: Compare the first element of neighboring arrays and sort them, putting them into a results array.  3. Return results when all elements have been copied. | O(N log(N)) - Non-recursive Merge function is O(N).  Recursive MergeSort is O(log(N)). Multiply the two to get its worst-case run time. | O(N) - creates separate results array as data is being merged | Stable: elements maintain original positions with respect to each other. | Useful in databases.  Useful when additional data may arrive during/after sorting.  Used by Safari/Firefox in their JS array method .sort()
Quick | Divides the array into three parts, pivot, leftP, and rightP. The pivot is considered sorted because it’s one item. Recursively call quick sort on the left and right partitions to sort those elements as well. | 0(N^2) - partitions each array recursively. | 0(log(N)) | Unstable:  we swap non-adjacent elements without respect to their original positions.  (Relative order of equal sort items is not preserved) | Good in virtual memory environment.  The built-in sort for C programming languages, Java, Python.  Works better for caching environments.  Gets tripped up on data sets with similar values (merge would be better)

</details>

<details>
<summary>Distribution Sorting Methods</summary>

Name | Description | BigO Time | Big0 Space | Stability | Use Cases
--- | --- | --- | --- | --- | ---
Bucket | Distribute elements into buckets(arrays) based on their value.  Sort elements in each bucket using a sorting method(insertion).  Put all the elements back into the original array.| O(N^2) | O(N) - making another array | Stable: if we use insertion sort. | Dense data, when values in your starting array are relatively close.  (But not too close, or they will all end up in one bucket.


</details>

<details>
<summary>Search Algorithms</summary>

Name | Description | BigO Time | Big0 Space | Stability | Use Cases
--- | --- | --- | --- | --- | ---
Binary Search | Starts comparing the search element with the middle element in the list.  If both match, then return the index. Otherwise, check whether the search element is smaller or larger than the middle element in the list.  If the search element is smaller, then we repeat the same process for the left sublist of the middle element.  If the search element is larger, then we repeat the same process for the right sublist of the middle element.  Repeat this process until we find the search element in the list or until we’re left with a sublist of only one element. And if that element also doesn't match with the search element, then return -1. | O(log n) - we reduce the number of elements in the array we’re considering by ½ each time. | O(1) - no new array needed| Stable | Array must be sorted.  Can be implemented on different data types such as numbers and strings


</details>
