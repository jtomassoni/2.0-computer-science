# Big O Notation

- algorithm speed isn't measured in seconds, but in growth of the number of operations
- in coding, we use the idea of the “worst-case scenario” to compare the efficiency of different algorithms
- In software development, Big O focuses on the efficiency of an algorithm as its input increases. It’s used to describe time complexity or space complexity:
    - **Time complexity** refers to the amount of time an algorithm takes to run (not specifically in increments of time, but in number of basic steps to execute relative to the size of the data set it's working on)
    - **Space complexity** refers to the amount of memory or RAM an algorithm needs to run.
    
    
![BigOChart](https://user-images.githubusercontent.com/68978118/105875138-a7e09080-5fba-11eb-8e38-fd0be9b8cb38.png)


## Five Classes of Complexity

### 0(1) Constant
Static or constant, complexity stays the same no matter the input.

<details>
<summary>Code Example</summary>

```jsx
// Example 1
function helloWorld {
    console.log('hello world')
}

// Example 2
let people = {
    instructor: "jimmy",
    student: "doug",
    boss: "shanaz"
}
people.instructor
=> "jimmy"
```

</details>

### O(N) Linear
As the input sizes increase, the processing time increases linearly or once for each input (for loop).

<details>
<summary>Code Example</summary>
```jsx
// Example 1
function iterate (arr) {
    arr.forEach(item => console.log(item))
}

// Example 2
function iterateLoop (arr) {
    for (let i = 0; i < arr.length; i++) {
        console.log(arr[i])
    }
}

```
</details>


### O(N^2) Quadratic
Performance is directly proportional to the squared size of the input data (nested loops/loops through for each item).

<details>
<summary>Code Example</summary>
```jsx
function consoleLogLots (arr) {
    for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr.length; j++) {
            console.log(arr[i], arr[j])
        }
    }
}

// ..for arr[1, 3], this function will print:

[1, 1]
[1, 3]
[3, 1]
[3, 3]


```


</details>

### O(log n) Logarithmic
Running time grows in proportion to the logarithm of the input size.
<details>
<summary>Code Example</summary>

```jsx
function binarySearch(arr, item, first = 0, last = null) {
    if (!last) last = arr.length
    let midpoint = Math.floor((last - first) / 2) + first
    if (arr[midpoint] === item) return midpoint
    if (arr[midpoint] > item) return binarySearch(arr, item, first, midpoint)
    if (arr[midpoint] < item) return binarySearch(arr, item, midpoint, last)
}

// Let’s say we want to find the value 5 in arr[1, 3, 5, 7, 9, 11, 13]. 
// The function above would run three times instead of the seven that we would need if we iterated through the entire array

```


</details>


### O(N!) Factorial
Calculates all possible permutations
<details>
<summary>Code Example</summary>


</details>
### Looking at Time Complexity

The `N` variable is the size of the input, or more plainly, the number of items being sorted. As we move from left to right across the table, we’re moving from very efficient runtimes like `O(1)` and `O(log(N))` to extremely inefficient runtimes like `O(N!)`. Stay away from the ones on the right!

## Comparing Complexity Cases

Input(N) | 0(1) | 0(log(N)) | O(N) | O(N^2) | O(N!)
--- | --- | --- | --- | --- | ---
1 | 1 | 1 | 1 | 1 | 1 
10 | 1 | 3 | 10 | 100 | 3,628,800
40 | 1 | 5 | 40 | 1,600 | 8.16e+47
80 | 1 | 6 | 80 | 6,400 | 80!
600 | 1 | 9 | 600 | 360,000 | 800!


## Visualizing the Difference

Click each line for a graphical representation.


<details>
<summary>Constant Complexity: O(1)</summary>
![Constant Complexity](https://user-images.githubusercontent.com/68978118/105875533-23424200-5fbb-11eb-96d9-2d3603205574.png)


</details>

<details>
<summary>Linear Complexity: O(N)</summary>
![Linear Complexity](https://user-images.githubusercontent.com/68978118/105875586-37863f00-5fbb-11eb-930c-17b8e5c1e53b.png)

</details>

<details>
<summary>Quadratic Complexity: O(N^2)</summary>
![Quadratic Complexity](https://user-images.githubusercontent.com/68978118/105875621-43720100-5fbb-11eb-899c-4dbfe0a5e39b.png)

</details>

<details>
<summary>Logarithmic Complexity: O(log(N))</summary>
![Logarithmic Complexity](https://user-images.githubusercontent.com/68978118/105875719-5dabdf00-5fbb-11eb-9541-5b2132a2f0c5.png)

</details>

<details>
<summary>Factorial Complexity: O(N!))</summary>
![Factorial Complexity](https://user-images.githubusercontent.com/68978118/105875767-6e5c5500-5fbb-11eb-81f0-b607fb2cf1de.png)

</details>


**What are the Big O time complexities of the following tasks?**

1. Peeling a bag of apples to make applesauce - Big O (N) - linear because the amount of steps needed to complete depends proportionally on the size of the input
2. Sorting a big deck of cards and removing all duplicates of each card you come across: flip over the first card and sort through the entire deck, removing duplicates of that first card. Then flip the second card and repeat that process. Big O(N^2) - quadratic because we’re repeating the steps of the algorithm twice for each input
3. Throwing an apple in the trash - Big O (1) - constant
4. Flipping through a phone book to find someone’s number. Start at the middle and flip forward or backward depending on how close you are to their last name - Big O (log(N)) - logarithmic because we’re cutting the problem in half each time

You could be asked to look at an algorithm, determine its Big O complexity, and give your reasoning. If so, keep the following considerations in mind:

- Does the function have to go through an entire list? If so, there’s an `N` in that Big O class somewhere.
- Are there nested loops? That might give you `O(N^2)` (or worse).
- Does the function break the list into smaller chunks? You could have `O(log(N))`.
- Is the amount of work the same, regardless of the size of the data set? You might have `O(1)`.
