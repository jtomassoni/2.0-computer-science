# **What Is Recursion?**

- Put simply, recursion is when a function calls itself
- We know a function can call upon other functions to achieve its goal, but it can also call upon itself
- When functions start getting too big to read clearly and test easily, you split them up into smaller functions that each perform part of the larger task
- A recursive function will achieve a small part of the larger task, then pass the partially completed problem to another call of itself
- Example

```jsx
// This function just counts down from a given number to zero
function countDown(num){
  if(num < 0){
    return;
  }
  console.log(num)
  return countDown(num - 1)
}
```

- We can break down the process of a recursive function into three steps:
    - **Base case**: establishes when the recursive function can finally return a specific value and no longer needs to continue calling itself to find that value

        ```jsx
        function countDown(num)
          if(num < 0){
            return;
          }
        ```

    - **Action**: the function actually executing

        ```jsx
        function countDown(num){
          if(num < 0){
            return;
          }
          console.log(num);
        }
        ```

    - **Recursive case**: The function is called again but with the assurance that progress is being made toward the base case.

        ```jsx
        function countDown(num){
          if(num < 0){
            return;
          }
          console.log(num);
        // the (num - 1) helps to make progress
          return countDown(num - 1);
        }
        ```

    - Longer Explanation

    # **Writing Recursive Functions**

    There are four basic steps to writing a recursive function:

    1. Define your function and parameters.

        ```jsx
        function sumArrayOfNums(arr, index = 0, sum = 0){
        }
        ```

    2. Define your base case and return the computed result.

        ```jsx
        function sumArrayOfNums(arr, index = 0, sum = 0){
          if(index === arr.length){
              return sum;
          }
        }
        ```

    3. Perform the action step.

        ```jsx
        function sumArrayOfNums(arr, index = 0, sum = 0){
          if(index === arr.length){
              return sum;
          }
          sum += arr[index];
        }
        ```

    4. Return the function with new arguments to make progress toward the base case.

        ```jsx
        function sumArrayOfNums(arr, index = 0, sum = 0){
          if(index === arr.length){
              return sum;
          }
          sum += arr[index];
          return sumArrayOfNums(arr, index + 1, sum);
        }
        ```

    # **Recursive Helper Functions**

    - Sometimes, recursive functions can only get by with a little help from recursive helper functions
    - They help the recursive function branch out in several different directions
        - You’ll often want a parent scope to hold onto the progress made by each recursive call
    - It can be useful to include a non-recursive parent function in which you define and call a recursive function
    - Including a non-recursive parent function can also eliminate the need for the recursive function within it to hold onto information with parameters
    - This pattern is especially useful for combination problems, when each recursive function might be calling itself several times with different inputs
    - A parent function can hold a list of all the combinations, and each recursive call can post its end result to the list held in the parent scope

    Here’s what `sumArrayOfNums()` would look like with a helper function:

    ```jsx
    function sumArrayOfNums(arr){
        let index = 0;
        let sum = 0;
        // Notice the lack of parameters in rSum!
        function rSum(){
          if(index === arr.length){
            return sum;
          }
          sum += arr[index];
          index++;
          return rSum();
        }
        // Once you’ve defined the helper function, make sure you call it!
        return rSum();
      }
    ```

    # **Why Do We Use Recursion**

    - Recursion is like looping, which uses iterations
    - For simple problems, a for loop is just as good as a recursive function
    - More complex problems will make more sense to solve recursively than iteratively
    - Recursion is written more cleanly and with less code, especially when a problem gets larger and larger

    # **When to Use Recursion**

    - Recursion operates by breaking down a problem into smaller chunks
        - It is best used when there is a problem that can be broken down in this way
    - Use recursion in any situation that requires exploring multiple possibilities or paths, such as:
        - Calculating all possible combinations of elements
        - Checking all possible routes between two destinations
    - Recursion provides the simplest solution to problems like these by allowing a function to continue through each possibility in a new recursive call.
