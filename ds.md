## Data Structures

1. Lists

   - Definition: An ordered collection of items which can be of different types.
   - Operations: Insertion, Deletion, Traversal, Searching.
   - Types: Array List, Linked List (Singly, Doubly, Circular).
   - Use Cases: Implementing stacks, queues, and other abstract data types.
   - Examples: Task manager, Social media feed.

2. Arrays

   - Definition: A collection of items stored at contiguous memory locations.
   - Operations: Accessing, Updating, Traversal.
   - Types: One-dimensional, Multi-dimensional.
   - Use Cases: Storing fixed-size collections of data.
   - Examples: Image representation, Matrix operations.

3. Stacks

   - Definition: A linear data structure that follows the Last In First Out (LIFO) principle.
   - Operations: Push, Pop, Peek.
   - Use Cases: Function call management, Expression evaluation.
   - Examples: Undo functionality in text editors, Browser history.

4. Queues

   - Definition: A linear data structure that follows the First In First Out (FIFO) principle.
   - Operations: Enqueue, Dequeue, Peek.
   - Types: Simple Queue, Circular Queue, Priority Queue, Deque.
   - Use Cases: Task scheduling, Resource management.
   - Examples: Print queue, Customer service systems, Chat systems.

5. Heaps

   - Definition: A specialized tree-based data structure that satisfies the heap property.
   - Operations: Insertion, Deletion, Peek.
   - Types: Min-Heap, Max-Heap.
   - Use Cases: Implementing priority queues, Heap sort algorithm.
   - Examples: Job scheduling, Event management systems.

6. Trees
    - Definition: A hierarchical data structure consisting of nodes, with a single root node and child nodes.
    - Operations: Insertion, Deletion, Traversal (In-order, Pre-order, Post-order).
    - Types: Binary Tree, Binary Search Tree, AVL Tree, Red-Black Tree, B-Trees.
    - Use Cases: Representing hierarchical data, Searching and sorting.
    - Examples: File systems, Database indexing, Machine Learning.

7. Hash Tables

   - Definition: A data structure that maps keys to values for efficient data retrieval.
   - Operations: Insertion, Deletion, Searching.
   - Collision Resolution: Chaining, Open Addressing.
   - Use Cases: Implementing associative arrays, Caches.
   - Examples: Symbol tables in compilers, Database indexing.

8. Suffix Trees and Tries

   - Definition: Tree-like data structures used for storing a dynamic set of strings.
   - Operations: Insertion, Deletion, Searching.
   - Use Cases: Text processing, Autocomplete systems.
   - Examples: DNA sequence analysis, Search engines.

9. Graphs
    - Definition: A collection of nodes (vertices) connected by edges.
    - Operations: Insertion, Deletion, Traversal (DFS, BFS).
    - Types: Directed, Undirected, Weighted, Unweighted.
    - Use Cases: Network representation, Pathfinding algorithms.
    - Examples: Social networks, Transportation networks, Web page linking.


### Cache friendliness

Arrays and Array Lists are generally more cache-friendly than linked lists due to their contiguous memory allocation. This allows for better spatial locality, leading to fewer cache misses during traversal operations. In contrast, linked lists may lead to scattered memory access patterns, which can degrade performance due to increased cache misses.

Trees and graphs can vary in cache friendliness depending on their implementation. Balanced trees (like AVL or Red-Black trees) can be more cache-efficient than unbalanced trees due to their structured layout, but they still may not match the cache performance of arrays. Graphs, especially when represented using adjacency lists, can suffer from poor cache performance due to non-contiguous memory access patterns.