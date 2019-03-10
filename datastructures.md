# Comprehensive Data Structures Review
This document will go over general important information about the listed data
structures including some "interview-like" formatted questions with responses.
Coding samples will be included separately.

## Arrays
**Features**
- Store consecutively in memory
`arr = [a][b][c][d]`

- Indexing
`=> arr[0]
 => a
`

- Memory allocated at creation
`arr = new Array(4)`

- Depending on system, memory allocated could be filled with garbage or a
default value (like 0)

- Reallocation, i.e. increasing size, takes O(n) because you need to copy over
all the old data into the newly allocated array.  Generally the actual
allocation of memory as well as deallocation is treated as O(1). For example,
a resize function may double the original size of the array.
`resize(arr)
 => sizeof(arr) == 8
`

**Order Notation**
| Function | Average O-Notation | Worst O-Notation |
|:--------:| ------------------:| ----------------:|
| Insert   | O(n)               | O(n)             |
| Access   | O(1)               | O(1)             |
| Delete   | O(n)               | O(n)             |
| Search   | O(n)               | O(n)             |
Space Complexity: O(n)
Pros:
Cons:

## Linked Lists
Features:
Order Notation (table):
Pros:
Cons:

## Trees
Features:
Order Notation (table):
Pros:
Cons:

## Maps
Features:
Order Notation (table):
Pros:
Cons:

## Sets
Features:
Order Notation (table):
Pros:
Cons:

## Hash Maps/Sets
Features:
Order Notation (table):
Pros:
Cons:
