[https://career.guru99.com/top-50-data-structure-interview-questions/](https://career.guru99.com/top-50-data-structure-interview-questions/)

- Linked Lists

    ## **Linked Lists**

    Lists that store data inside of nodes that point to each other.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/7-Diagram.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/7-Diagram.png)

    Linked lists are a foundational data structure used by many complex data structures.

    The key component of a linked list is a **node**. Other advanced data structures use nodes, too, but in a linked list specifically, a node is a unit containing two things at the same time:

    - A `data` property that stores a value.
    - A `next` property, sometimes called a “pointer,” that points to the next item in the list.

    In the case of linked lists, the only exception to this rule is the very last node. It doesn’t need a pointer, so it’s known as a “null next node” (or more simply, “the tail”).

    # **Linked Lists: Pros and Cons**

    Linked lists sound pretty sweet, don’t they? You can keep growing and adding nodes — or, in the case of our real estate analogy, buildings — in any manner you please.

    But linked lists do present some challenges:

    - They take up more space than arrays because you have to store both the pointers AND the data (in terms of our real estate analogy, you have to hire building managers — another expense).
    - It can take more time to access a linked list because the data set isn’t read as one continuous chunk (you have to travel all over the city to reach your buildings).
    - You can’t access a particular node in a linked list without starting from the top and moving sequentially until you find it (unlike in an array, where you can quickly find a value based on its index).

    [Time Complexity](https://www.notion.so/ea091052dec148c2a2e98c9d5912f828)

- Stacks

    ## **Stacks**

    Lists of ordered values in which the first item in is the last item out.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/5-Push-Pop.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/5-Push-Pop.png)

- Queues

    ## **Queues**

    Lists of ordered values in which the first item in is the first item out.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/6-Enqueue.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/6-Enqueue.png)

- Hash Tables

    ## **Hash Tables**

    List-like structures that use a hash function to generate keys for values.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/english/11-Keys-Indices-Diagram.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/english/11-Keys-Indices-Diagram.png)

    A hash function takes in a key, such as a string or integer, for a data record (often a key-value pair) and returns an integer memory address, or an index in a table where that record can be stored. In other words, it maps some key from the very large universe of possible keys to a much smaller range of possible indices in a hash table.

    Chaining is another method of resolving collisions. Chaining means that each slot of the table can contain what is considered to be a “bucket,” which can hold more than one record. These buckets are data structures into which you can insert as many keys/records as you like.

    - 

    Hash tables are an important concept with a lot of related vocabulary! Let’s recap:

    - **Hash table**: A data structure that maps a key to an index in a table.
    - **Hash function**: Takes a key, scrambles it, and outputs an index to be used in a hash table.
    - **Collisions**: When a hash function generates the same index for two different values.
    - **Open addressing**: A resolution for collisions that uses probing (searching for other indices in the table).
    - **Closed addressing**: A resolution for collisions that creates “chains” of other data structures at each index.
- Sets

    ## **Sets**

    Similar to an array, but can only contain unique values.

    ![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48199fc6-8802-4b29-9b8b-140c0a5b48f7/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/48199fc6-8802-4b29-9b8b-140c0a5b48f7/Untitled.png)

    The following methods are commonly built into sets:

    [Common Set Methods](https://www.notion.so/6d12603ffe87488a8e60e884c8729876)

- Binary Trees

    ## **Binary Trees**

    Node-based structures that store values using left and right pointers.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/8-Diagram.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/8-Diagram.png)

- Trees

    ## **Trees**

    Tree structures in which nodes can store lists of child nodes; almost always used for strings.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/10-Root-Children-Diagram.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/10-Root-Children-Diagram.png)

- AVL Trees

    ## **AVL Trees**

    A binary tree that's balanced. Notice how each side of this tree is a similar height? That means it's balanced.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/8-Diagram.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/8-Diagram.png)

- Graphs

    ## **Graphs**

    Collections of nodes and edges in which nodes store data and edges represent connections between data.

    ![https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/9-Diagram.png](https://ga-instruction.s3.amazonaws.com/assets/tech/computer-science/intro-data-structures/9-Diagram.png)
