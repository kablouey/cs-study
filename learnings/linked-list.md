---
tags:
  - alg
---
# Linked List
## Definition
A linked list is a [[data-structure|data structure]] in which each element is implemented as a node containing the element and a pointer to the next node.
The head pointer points to the start of the list.
Variations include a tail pointer, as well as doubly linked lists in which nodes point to both the previous and next node in the list.

## Insertion
Insertion is achieved by pointing the node previous to the insertion point to the new node, and the new node to the node next in line.

## Deletion
To delete a node, redirect the preceding node to the node following the node-to-be-deleted, effectively skipping that node.

## Pros
- Dyamic sizing means resizing is fast and inexpensive
- Easy to insert/delete due to node structure

## Cons
- Random access is not possible. As a result search algorithms based on elements like binary search are not possible. Specific elements must be searched from head-tail or tail-head, i.e. iterated through.
- Is more complex than an array, through the inclusion of pointers  and as such takes up more memory
