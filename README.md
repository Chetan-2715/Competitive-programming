# CP / DS Lab Practicals – Python

This repository contains solutions for all 15 practicals from the CP/DS Lab Manual.
All programs are written in Python and organized in Jupyter Notebook cell format.

---

## 📘 Practical List

# Practical 1 – Arrays

## Aim  
To study problems on Array.

## Theory  
An array is a fundamental data structure that stores elements of the same data type at contiguous memory locations. This allows efficient computation of an element’s position using an offset from the base address. Arrays support fast access using indexing and are widely used for data organization, searching, and manipulation.

### Array in Python  
In Python, arrays are created using the built-in `array` module.  
Syntax:
    array(data_type, value_list)

### Key Operations in Python Arrays  

#### 1. Creating an Array  
Arrays are created by specifying the data type and initial values.  

#### 2. Adding Elements  
- **insert()** → Inserts an element at a specified index.  
- **append()** → Adds an element at the end of the array.

#### 3. Accessing Elements  
Elements are accessed using indices inside square brackets `[]`.  
Index must be an integer.

#### 4. Removing Elements  
- **remove()** → Removes the first occurrence of a value.  
- **pop()** → Removes and returns an element.  
  - Without arguments → removes the last element.  
  - With index → removes element at that index.

#### 5. Array Slicing  
Slicing retrieves a part of the array using the colon operator `:`.  
Examples include:
- `[:index]` → Start to index-1  
- `[index:]` → Index to end  
- `[start:end]` → Start to end-1  
- `[::-1]` → Reverse array  
- `[:]` → Full array

#### 6. Searching  
Python provides the **index()** method to search for an element.  
It returns the index of the first occurrence.

---
# Practical 2 – Matrix

## Aim  
To study problems on Matrix.

## Theory  
A matrix is a structured collection of numbers arranged in a rectangular format of rows and columns. Matrices play a crucial role in various fields such as engineering, physics, statistics, computer graphics, and machine learning. They are heavily used for representing datasets, solving linear equations, performing transformations, and handling multi-dimensional data.

A matrix containing *m* rows and *n* columns is called an **m × n matrix**.

### Creating a Matrix in Python  
In Python, a matrix can be represented using a **list of lists**, where each inner list represents a row of the matrix.

### Assigning Values  
Matrix elements can be modified by referring to their row and column index. Python follows zero-based indexing, meaning the first row/column has index 0.

### Accessing Values  
To access any element, the row index and column index are provided inside square brackets.  
For example, `matrix[row][column]` refers to the specific element stored at that position.

---

# Practical 3 – String

## Aim  
Problems on String.

## Theory  
A string is a fundamental data structure in Python that represents a sequence of characters.  
It is an **immutable** data type, meaning once a string is created, its contents cannot be changed directly. If modification is needed, a new string must be created and assigned.

Strings are used for storing and manipulating text-based data such as names, addresses, and messages. Python does not have a separate character data type; instead, a single character is simply a string of length one.

### Creating a String  
Strings can be created using:
- Single quotes `' '`
- Double quotes `" "`
- Triple double quotes `""" """` for multi-line strings

### Accessing Characters (Indexing)  
String elements can be accessed using indexing:
- **Positive indexing** (starting from 0 for the first character)
- **Negative indexing** (e.g., -1 refers to the last character, -2 to the second last)

Accessing an index out of the string's range results in an `IndexError`.  
Only integers are valid indices; using floats or other types leads to a `TypeError`.

### String Slicing  
Slicing allows accessing a range of characters using the colon operator `:`.  
It returns a substring starting from the first index and ending one position before the last index.

Example:  
`s[1:4]` returns characters from index 1 to 3.

### Immutability of Strings  
Python strings are immutable.  
- Updating or deleting individual characters is **not allowed**.  
- Deleting the entire string is allowed using the `del` keyword.  

Workarounds to “modify” a string:
1. Convert the string into a list, modify the element, then convert back to a string.  
2. Use slicing to rebuild the string around the updated character.

### Case Changing (Built-in Functions)  
Python provides several built-in functions for changing the case of characters:
- `lower()` → Converts all characters to lowercase  
- `upper()` → Converts all characters to uppercase  
- `title()` → Capitalizes the first letter of each word  
- `swapcase()` → Swaps uppercase and lowercase  
- `capitalize()` → Capitalizes only the first character of the string
---

# Practical 4 – Searching and Sorting

## Aim  
To study Searching and Sorting techniques.

## Theory  

### Searching Algorithms  
Searching algorithms are designed to locate or retrieve an element from a data structure.

#### 1. Sequential Search (Linear Search)  
In Linear Search, elements of the list or array are checked one by one sequentially until the required value is found or the end of the list is reached.

#### 2. Interval Search (Binary Search)  
Binary Search is an efficient searching method used only on **sorted** data.  
The search space is repeatedly divided into halves by comparing the target value with the middle element.  
- If the target matches the middle element → search ends  
- If the target is smaller → search continues in the left half  
- If larger → in the right half  

### Sorting Algorithms  
A sorting algorithm arranges elements of an array or list in a defined order (ascending or descending).

#### 1. Selection Sort  
The algorithm divides the array into two parts:
- The **sorted** part at the beginning  
- The **unsorted** part at the end  
In each iteration, the smallest element from the unsorted part is selected and swapped with the leftmost unsorted element.

#### 2. Bubble Sort  
This simple algorithm repeatedly compares adjacent elements and swaps them if they are in the wrong order.  
This process continues until the array is completely sorted, though it is inefficient for large datasets due to its high time complexity.

#### 3. Insertion Sort  
This method builds the final sorted array one item at a time.  
The structure is conceptually divided into:
- a **sorted** section  
- an **unsorted** section  
Each new element is taken from the unsorted part and inserted at the correct position in the sorted part.

#### 4. Merge Sort  
A classic **Divide and Conquer** algorithm.  
The array is split into two halves recursively until each subarray contains a single element.  
Then the subarrays are merged together in a sorted order.

#### 5. Quick Sort  
Another Divide and Conquer algorithm where a **pivot** element is selected.  
Elements smaller than the pivot are placed on its left, and larger elements on its right.  
This partitioning is applied recursively until the entire array is sorted.

#### 6. Heap Sort  
A comparison-based sorting technique based on the **Binary Heap** data structure.  
It is similar to Selection Sort:
- The maximum (or minimum) element is extracted from the heap  
- Placed in its correct position  
- The heap is rebuilt  
This continues until the array is fully sorted.
---

# Practical 5 – Linked List

## Aim  
To study problems on LinkedList.

## Theory  
A linked list is a linear data structure in which data elements are stored in separate memory blocks called nodes.  
These nodes are connected through pointers rather than being stored in contiguous memory locations.  
Each node typically contains:
- A **data** field that stores the value.
- A **reference (link)** to the next node in the sequence.

This structure allows dynamic memory allocation and efficient insertions or deletions.

### Types of Linked Lists  

#### 1. Singly Linked List  
The simplest form of linked list.  
Each node contains:
- Data  
- Pointer to the **next** node  

Traversal is one-directional (forward only).  
The last node’s next pointer contains **NULL**.

Illustration:
Head → A → B → C → D → NULL

#### 2. Doubly Linked List  
Also known as a two-way linked list.  
Each node contains:
- Data  
- Pointer to the **next** node  
- Pointer to the **previous** node  

It allows traversal in **both forward and backward** directions.  
The first node’s previous pointer and last node’s next pointer are **NULL**.

#### 3. Circular Linked List  
In this structure, the last node points back to the first node, forming a **circular chain**.  
There is no fixed beginning or end.  
Traversal can continue indefinitely until the starting node is reached again.

#### 4. Doubly Circular Linked List  
A hybrid of Doubly Linked List and Circular Linked List.  
Each node has:
- Data  
- Next pointer  
- Previous pointer  

The last node’s next pointer points to the **first** node,  
and the first node’s previous pointer points to the **last** node.  
No pointer contains NULL.

---

# Practical 6 – Binary Trees

## Aim  
To study problems on Binary Trees.

## Theory  

### What is a Binary Tree?  
A Binary Tree is a hierarchical data structure in which each node can have **at most two children**.  
These children are commonly referred to as the:
- **Left child**
- **Right child**

Binary Trees are widely used in applications such as expression parsing, searching, sorting, and hierarchical data representation.

### Binary Tree Representation  
A Binary Tree is represented using a pointer to the **root** node.  
If the tree is empty, the root is assigned **NULL**.

Each node in a Binary Tree typically contains:
- **Data** – the value stored in the node  
- **Pointer to the left child**  
- **Pointer to the right child**  

This structure allows recursive algorithms to work efficiently on trees.

### Basic Operations on Binary Trees  
A Binary Tree supports the following operations:
- **Insertion** of a new node  
- **Deletion/Removal** of an existing node  
- **Searching** for a specific value in the tree  
- **Traversal** of all nodes using methods such as:
  - Inorder Traversal  
  - Preorder Traversal  
  - Postorder Traversal  
  - Level Order Traversal (using queues)
---

# Practical 7 – Binary Search Tree (BST)

## Aim  
To study problems on Binary Search Tree.

## Theory  

### What is a Binary Search Tree?  
A Binary Search Tree (BST) is a special type of binary tree that follows three strict properties:

1. The **left subtree** of a node contains only nodes with values **less** than the node’s value.  
2. The **right subtree** of a node contains only nodes with values **greater** than the node’s value.  
3. Both the left and right subtrees must themselves be valid Binary Search Trees.

This structured ordering enables efficient searching, insertion, and deletion operations.

---

### Insertion in a Binary Search Tree  
A new value is always inserted at a **leaf node**, ensuring BST properties are maintained.

**Steps for insertion:**
1. Start from the root and compare the new key **X** with the current node value **val**.  
2. If **X < val**, move to the left subtree.  
3. If **X > val**, move to the right subtree.  
4. Continue until a leaf node is reached.  
5. Insert **X** as the left or right child depending on the comparison.

---

### Searching in a BST  
To search for a value **X**:
1. Start at the root and compare **X** with the root's value.  
2. If equal → value found.  
3. If smaller → go to left subtree.  
4. If larger → go to right subtree.  
5. Repeat until the key is found or traversal ends.  
If traversal ends without a match → the key does not exist in the tree.

---

### Deletion in a BST  
Deleting a node in a BST involves **three main cases**:

#### Case 1: Deleting a Leaf Node  
- The node is simply removed since it has no children.

#### Case 2: Deleting a Node with One Child  
- Replace the node with its child.  
- Delete the child node (now redundant).

#### Case 3: Deleting a Node with Two Children  
- Find the **inorder successor** (minimum value in the right subtree).  
- Replace the target node’s value with the successor’s value.  
- Delete the inorder successor (which will be either a leaf or have one child).

---

### Traversal Techniques in BST  

#### Inorder Traversal  
Left subtree → Root → Right subtree  
- Produces the nodes of a BST in **sorted order**.

#### Preorder Traversal  
Root → Left subtree → Right subtree  

#### Postorder Traversal  
Left subtree → Right subtree → Root  

---

# Practical 8 – Greedy Technique

## Aim  
To study Greedy Technique.

## Theory  

### What is a Greedy Algorithm?  
A Greedy Algorithm is a strategy used to solve optimization problems by making the **locally optimal choice** at each step, with the hope that these immediate choices will eventually lead to a globally optimal solution.  
It focuses on choosing the option that appears best **at the current moment**, without reconsideration or backtracking.

Greedy techniques are effective in problems where the optimal local decisions lead to an optimal global result.

---

### Characteristics of a Greedy Algorithm  
For a problem to be suitable for the Greedy approach, the following characteristics are generally expected:

1. **Resource Ordering**  
   There must be a basis for arranging or ordering elements (e.g., profit, value, weight).

2. **Local Optimization**  
   At each step, the algorithm selects the **best possible option available** (e.g., taking the item with the maximum value/weight ratio in Fractional Knapsack).

3. **Feasible and Safe Choice**  
   Each choice must maintain feasibility of the overall solution.

4. **Irrevocable Decisions**  
   Once a choice is made, it cannot be changed or undone.

---

### Use of Greedy Algorithms  
Greedy methods are commonly applied in problems involving **minimization** or **maximization**. Popular applications include:

- **Scheduling and Resource Allocation**  
  Efficiently allocating time or resources to maximize throughput.

- **Graph Algorithms**  
  Such as finding shortest paths or minimum spanning trees.  
  (Examples include Dijkstra’s Algorithm, Prim’s Algorithm, and Kruskal’s Algorithm.)

- **Coin Change Problem**  
  Making change for a given amount using the fewest number of coins.

- **Huffman Coding**  
  Constructing a prefix-free optimal code used in compression.

---

### Important Note  
The greedy approach **does not always guarantee the optimal solution** for all optimization problems.  
However, for many well-defined problems, it is efficient, simple, and produces correct or near-optimal results.

---
# Practical 9 – Backtracking

## Aim  
To study problems on Backtracking.

## Theory  

### What is Backtracking?  
Backtracking is a general algorithmic problem-solving technique used to explore multiple possible solutions by building them step-by-step.  
If at any point a chosen path leads to a **dead end** or an invalid state, the algorithm **reverts (backtracks)** to the previous step and tries a different option.

It is widely used in problems that require exploring different configurations or combinations, such as:
- Maze solving  
- Sudoku solving  
- N-Queens problem  
- Generating permutations and combinations  

Backtracking systematically searches through all possible solution paths until it finds one that satisfies the problem’s constraints.

---

### How Backtracking Works  
The working of a backtracking algorithm can be visualized using a **state-space tree**, where each node represents a state of the problem.

- **Initial State (IS):**  
  The starting point of the algorithm where the first decision is made.

- **Checkpoints (C):**  
  Intermediate states where choices are made (e.g., choosing a row or a column in N-Queens).  
  Each checkpoint branches into multiple possible future states.

- **Terminal Nodes (TN):**  
  States where no further decisions can be made.  
  These are base cases in recursion.  
  A terminal node may represent:
  - A **valid solution**, or  
  - An **invalid/dead-end** (requiring backtracking)

### Backtracking Action  
At each checkpoint:
1. A decision is made and the algorithm moves forward.  
2. If the terminal state reached is **invalid**, the algorithm reverses its last choice (backtracks) and tries the next available option.  
3. This continues until:
   - A valid solution is found, or  
   - All possibilities are exhausted.

Backtracking ensures that every possible path is explored in a structured manner, making it a powerful technique for solving computational search problems.

---

# Practical 10 – Stack & Queue

## Aim  
To study problems on Stack & Queues.

## Theory  

### Stack  
A **Stack** is a linear data structure that follows the **Last-In, First-Out (LIFO)** principle.  
This means the element inserted last is the first one to be removed.

Key Operations:
- **Push**: Adding an element to the top of the stack.  
  In Python, `append()` is used to push an element to the end of the list.
- **Pop**: Removing the topmost element.  
  In Python, `pop()` removes and returns the last element from the list.

Stacks are efficient when operations occur at only one end.

#### Applications of Stack  
- Many CPUs use stacks internally to evaluate expressions and manage registers.  
- Function calls and return addresses in programming languages are managed using stacks.  
- The C++ runtime system uses a stack-based approach for execution flow.

---

### Queue  
A **Queue** is a linear data structure that operates on the **First-In, First-Out (FIFO)** principle.  
This means the first element inserted is the first one to be removed.

Key Operation:
- **Pop/Dequeue**: In Python’s list-based queue implementation, `pop(0)` removes the first element (front of the queue).

Queues support insertion at the rear and deletion from the front.

#### Applications of Queue  
- Used in CPU instruction pipelines and microinstructions.  
- Essential in operating systems for managing processes, scheduling, buffering, and resource allocation.  
- Widely used in networking, simulations, and task management.
---

# Practical 11 – Heap

## Aim  
To study problems on Heap.

## Theory  

### What is a Heap Data Structure?  
A **Heap** is a specialized tree-based data structure in which the tree is a **complete binary tree**.  
This means every level of the tree is fully filled except possibly the last, which is filled from left to right.

Heaps are typically used to implement **priority queues**, where insertion and deletion are based on priority.

---

### Types of Heaps  

#### 1. Min Heap  
- The **root node** contains the **smallest** element in the heap.  
- Every parent node is smaller than or equal to its children.

#### 2. Max Heap  
- The **root node** contains the **largest** element in the heap.  
- Every parent node is greater than or equal to its children.

---

### Operations on Heap  

#### 1. Heapify  
The process of converting an arbitrary array into a heap structure.  
This is typically used in **heap construction** and **heap sort**.

#### 2. Insertion  
Inserting a new element into the heap while maintaining heap properties.  
The new element is placed at the bottom and then moved upward (heapify-up).  
Time Complexity: **O(log N)**

#### 3. Deletion  
Removing the **top element** (highest priority element):  
- In Min Heap → smallest element  
- In Max Heap → largest element  

After removal, the last element is moved to the top and heap properties are restored (heapify-down).  
Time Complexity: **O(log N)**

#### 4. Peek  
Retrieving the **topmost element** of the heap **without removing it**.  
Used to check the current highest-priority element.

---

# Practical 12 – Graph Data Structure

## Aim  
To study problems on Graph data structure.

## Theory  

### What is a Graph Data Structure?  
A **Graph** is a non-linear data structure consisting of a set of **vertices (V)** and a set of **edges (E)** that connect these vertices.  
A graph is commonly represented as:  
G(V, E)

Graphs allow relationships between data to be represented visually or structurally, making them useful for modeling various real-world systems.

---

### Components of a Graph  

#### 1. Vertices (Nodes)  
Vertices are the basic units of a graph.  
Each vertex may store data or represent an entity.  
Vertices can be:
- Labeled  
- Unlabeled  

#### 2. Edges (Arcs)  
Edges connect two vertices.  
In directed graphs, they represent **ordered pairs** of nodes.  
Edges may also be labeled or unlabeled depending on the application.

---

### Applications of Graphs  
Graphs are used extensively to solve real-world problems. They model:
- **City road maps** (pathfinding)
- **Network structures** like telephone lines or circuits
- **Social networks**  
  For example, Facebook uses vertices to represent people (with attributes like ID, name, gender, etc.)

Graphs are foundational in fields such as networking, biology, computer science, machine learning, and recommendation systems.

---

### Traversal Techniques  

#### Breadth First Search (BFS)  
- BFS explores the graph **level by level**.  
- It starts at a root node, explores all its neighbors, and then moves to the next level.  
- Used when the shortest path or minimal number of steps is required.  
- In graphs with cycles, a **visited array** is necessary to avoid infinite loops.  
- BFS uses a **queue** for traversal.

#### Depth First Search (DFS)  
- DFS explores as far as possible along one branch before backtracking.  
- It is similar to preorder traversal of a tree.  
- A **visited array** is used to avoid revisiting nodes.  
- A graph can have **multiple valid DFS orders**, depending on the path taken.

---

# Practical 13 – Trie Data Structure

## Aim  
To study Trie data structure.

## Theory  

### What is a Trie?  
A **Trie** (derived from the word *retrieval*) is a special type of **k-ary search tree** used for storing, searching, and retrieving strings efficiently.  
It is also known as a:
- **Prefix Tree**
- **Digital Tree**

A Trie stores strings such that **all strings sharing a common prefix branch from the same node**.  
This makes it ideal for handling large sets of strings and performing fast prefix-based searches.

Tries provide search times proportional to the length of the key rather than the number of keys, making them extremely efficient in applications such as autocomplete and spell checking.

---

### Structure of a Trie Node  
Each Trie node contains:
- **Multiple branches** representing characters of the alphabet  
- A boolean field **isEndOfWord** to mark whether a node corresponds to the final character of a valid string  

Nodes do not store entire keys; instead, characters are stored at different levels of the tree, with each path from the root to a leaf/prefix representing a string.

---

### Applications of Tries  
- **Building dictionaries** for managing large word sets efficiently  
- **Spell-checking** systems  
- **Autocomplete** and **search suggestion** engines  
- **Pattern matching** and prefix-related queries  
- **IP routing** (longest prefix match)

---

### Search Operation in a Trie  
Searching in a Trie is similar to insertion:

1. Start from the **root node**.  
2. Compare each character of the string with the corresponding branch.  
3. Move down to the next node if the branch exists.  
4. The search ends when:
   - All characters of the search key are matched.  
     - If **isEndOfWord = True**, the key exists.  
     - If **isEndOfWord = False**, the key is only a prefix, not a complete word.
   - A character does **not** have a matching branch.  
     - The search stops early and the key is not present.

---

# Practical 14 – Dynamic Programming

## Aim  
To study problems on Dynamic Programming.

## Theory  

### What is Dynamic Programming?  
Dynamic Programming (DP) is an optimization technique applied to recursive algorithms that face the problem of **overlapping subproblems**.  
If the same computation is performed repeatedly in recursion, DP improves efficiency by **storing and reusing** previously computed results.

DP significantly reduces time complexity—from exponential to polynomial—by eliminating redundant calculations.

DP is typically applied when:
- A problem can be divided into subproblems.
- Subproblems repeat (overlap).
- The optimal solution of the main problem depends on optimal solutions of subproblems.

DP is implemented using two key approaches:
- **Memoization (Top-Down):** Store results of expensive recursive calls.
- **Tabulation (Bottom-Up):** Build a table iteratively using base results.

---
# Practical 15 – Bit Manipulation

## Aim  
To study problems on Bit Manipulation.

## Theory  

### Operators  
Operators are special symbols used to perform operations on values and variables.  
The value on which an operator acts is known as the **operand**.

---

### Bitwise Operators  
In Python, bitwise operators operate on integers at the **binary level**.  
Each integer is converted into its binary representation, and the operation is performed **bit by bit**.  
The final result is returned in **decimal** format.

#### Bitwise Operator Table

| Operator | Name          | Description                                                                                            | Syntax  |
|----------|---------------|--------------------------------------------------------------------------------------------------------|---------|
| `&`      | Bitwise AND   | Result bit = 1 **only if** both operand bits are 1; otherwise 0.                                       | `x & y` |
| `\|`      | Bitwise OR    | Result bit = 1 if either operand bit is 1; otherwise 0.                                                | `x \| y` |
| `~`      | Bitwise NOT   | Inverts all bits of the operand (1 → 0, 0 → 1).                                                        | `~x`    |
| `^`      | Bitwise XOR   | Result bit = 1 if the operand bits are **different**; 0 if they are same.                             | `x ^ y` |

---

### Shift Operators  

#### Bitwise Right Shift (`>>`)
Moves the bits of the left operand to the **right** by the number of positions specified by the right operand.  
Effectively divides the number by 2 for each shift.

Example:  
`x >> n` shifts bits of `x` right by `n` positions.

#### Bitwise Left Shift (`<<`)
Moves the bits of the left operand to the **left** by the number of positions specified by the right operand.  
Effectively multiplies the number by 2 for each shift.

Example:  
`x << n` shifts bits of `x` left by `n` positions.

---

## 📌 Final Notes

This repository contains the complete set of programs and theoretical explanations for all 15 practicals covered in the CP/DS Laboratory syllabus. Each practical includes a clear aim, detailed theory, and corresponding Python implementations following the structure of the official lab manual.

The objective of this work is to help students understand core data structures and algorithms such as Arrays, Linked Lists, Trees, Graphs, Heaps, Tries, Dynamic Programming, Backtracking, Searching, Sorting, Stacks, Queues, Greedy methods, and Bit Manipulation through well-structured examples and clean implementations.

All programs are written in a simple, readable, and modular style to enhance learning and revision.

## 👨‍💻 Author  
Prepared by **Chetan 😎🔥**

## 📚 Acknowledgment  
This compilation is based on the concepts taught in the CP/DS Laboratory as per the syllabus and lab manual. Special thanks to the instructors and resources that guided the understanding of these fundamental concepts.

## ⭐ End of README  
Thank you for reading!  
Happy Coding 🚀🔥
