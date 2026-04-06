# Data Structures & Algorithms

## Core Concepts

### Arrays
- **Definition**: Contiguous memory storage for multiple elements of the same type
- **Time Complexity**: 
  - Access: O(1)
  - Insert/Delete: O(n)
- **Use Cases**: Random access, storing fixed collections
- **Pros**: Fast random access, cache friendly
- **Cons**: Fixed size (in some languages), expensive insertions/deletions

### Linked Lists
- **Definition**: Sequential collection of nodes, each containing data and reference to next
- **Time Complexity**:
  - Access: O(n)
  - Insert/Delete: O(1) if position known
- **Use Cases**: Dynamic collections, frequent insertions/deletions
- **Pros**: Dynamic size, efficient insertions/deletions
- **Cons**: Slower access, extra memory for pointers

### Hash Tables
- **Definition**: Maps keys to values using hash function
- **Time Complexity**: Average O(1), Worst O(n)
- **Use Cases**: Fast lookups, caching, counting occurrences
- **Key Concepts**:
  - Hash Function: Converts key to index
  - Collision Handling: Chaining or Open Addressing
  - Load Factor: Ratio of entries to buckets

### Binary Trees
- **Binary Tree**: Each node has at most 2 children
- **Binary Search Tree (BST)**: Left < Parent < Right
  - Average Time: O(log n)
  - Worst Case: O(n) if unbalanced
- **Balanced Trees**: AVL Tree, Red-Black Tree
  - Balanced Time: O(log n) guaranteed

### Graphs
- **Representations**: 
  - Adjacency Matrix: O(V²) space, O(1) edge lookup
  - Adjacency List: O(V+E) space, faster for sparse graphs
- **Traversal**:
  - DFS (Depth-First): Uses Stack
  - BFS (Breadth-First): Uses Queue
- **Shortest Path**: Dijkstra, Bellman-Ford, A*

## Sorting Algorithms

| Algorithm | Best | Average | Worst | Space | Stable |
|-----------|------|---------|-------|-------|--------|
| Bubble    | O(n) | O(n²)   | O(n²) | O(1)  | Yes    |
| Selection | O(n²)| O(n²)   | O(n²) | O(1)  | No     |
| Insertion | O(n) | O(n²)   | O(n²) | O(1)  | Yes    |
| Merge     | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| Quick     | O(n log n) | O(n log n) | O(n²) | O(log n) | No |
| Heap      | O(n log n) | O(n log n) | O(n log n) | O(1) | No |

## Searching Algorithms

### Linear Search
```
Time: O(n)
Space: O(1)
Best for: Unsorted data, small collections
```

### Binary Search
```
Time: O(log n)
Space: O(1) or O(log n) recursive
Requires: Sorted data
```

## Big O Cheat Sheet

```
O(1)     - Constant
O(log n) - Logarithmic
O(n)     - Linear
O(n log n) - Linearithmic
O(n²)    - Quadratic
O(n³)    - Cubic
O(2ⁿ)    - Exponential
O(n!)    - Factorial
```

## Key Principles

1. **Trade-offs**: Time vs Space
2. **Asymptotic Analysis**: Ignore constants and lower-order terms
3. **Worst Case**: Analyze worst-case scenarios
4. **Scalability**: How does performance scale with larger inputs?
5. **Problem Constraints**: Choose algorithm based on constraints

## Problem-Solving Approach

1. Understand the problem completely
2. Identify inputs and outputs
3. Consider edge cases
4. Start with brute force solution
5. Identify patterns and optimize
6. Implement efficiently
7. Test thoroughly

---
**Last Updated**: 2026-04-05
