# Comprehensive Data Structures Review
This document will go over general important information about the listed data
structures including some "interview-like" formatted questions with responses.
Coding samples will be included separately.

## Arrays
**Notes**
- Store contiguously in memory (allocated as a contiguous block of memory)

`arr = [a][b][c][d]`

- Indexing

`=> arr[0]
 => a
`

- Memory allocated at creation

`arr = new Array(4)`

- Depending on system, memory allocated could be filled with garbage or a
default value (like 0).

**Order Notation**
- Note: arrays lack other functionality of data structures like resizing which
is why other functions are missing.  Everything is constant time but that is on
the assumption that you know the index of where you want to access.

| Function   | Average O-Notation | Worst O-Notation |
|:----------:| ------------------:| ----------------:|
| access     | O(1)               | O(1)             |

**Space Complexity**
- Initial: O(n)
- Average: O(n)

## Vectors
**Notes**
- Underneath, a vector is just an array with the ability to edit the contents
more flexibly.
- Reallocation, i.e. increasing size, takes O(n) because you need to copy over
all the old data into the newly allocated array.  Generally the actual
allocation of memory as well as deallocation is treated as O(1). For example,
a resize function may double the original size of the array.

`vec = Vector(4)
 resize(vec)
 => sizeof(vec) == 8
`

**Order Notation**

| Function   | Average O-Notation | Worst O-Notation |
|:----------:| ------------------:| ----------------:|
| access     | O(1)               | O(1)             |
| push_back  | O(1)               | O(n)             |
| pop_back   | O(1)               | O(1)             |
| insert     | O(n)               | O(n)             |
| erase      | O(n)               | O(n)             |
| find       | O(n)               | O(n)             |

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Linked Lists
**Notes**
- Linked lists are typically designed as node objects with two components:
the value of the node and a pointer to the next node.
- Lists are also typically set up as doubly linked lists with pointers going
to and from nodes with a head and tail pointer.
- Lists are different vectors because you cannot index into them and must
traverse the length of the data structure to find the element you're looking
for.  However, because the nodes are connected via pointers, lists benefit
from quick insert and removal at the front and back of the list.
- Unlike arrays, lists are most likely not stored contiguously in memory.
- It is also possible that lists will take up more of a memory footprint
to allocate the nodes and pointers compared to allocating memory for an array.

**Order Notation**

| Function     | Average O-Notation | Worst O-Notation |
|:------------:| ------------------:| ----------------:|
| access       | O(n)               | O(n)             |
| push_back    | O(1)               | O(1)             |
| pop_back     | O(1)               | O(1)             |
| pop_front    | O(1)               | O(1)             |
| push_front   | O(1)               | O(1)             |
| insert       | O(n)               | O(n)             |
| erase        | O(n)               | O(n)             |
| find         | O(n)               | O(n)             |

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Trees
**Notes**
- Trees, like linked lists, are generally designed as node objects, but instead
of being ordered linearly, there is a hierarchical structure.  There is a root
node that then will have children.  While trees could technically have any
number of children, binary trees, where each node has a maximum of two children,
is the most popular use of trees.
- Binary search trees, BSTs, have the unique feature in that for every node in
the tree, all children to the left of the node is smaller than it and all
children to the right of the node is larger than it.
- Full binary trees are where every node has either no children or two children.
- All trees are graphs but not all graphs are trees as graphs can have cycles
in them and trees may not.

**Order Notation**

| Function   | Average O-Notation      | Worst O-Notation      |
|:----------:| -----------------------:| ---------------------:|
| insert     | O(log n)                | O(log n)              |
| erase      | O(log n)                | O(log n)              |
| find       | O(log n)                | O(log n)              |

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Maps
**Notes**

**Order Notation**
- See Trees

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Sets
**Notes**

**Order Notation**
- See Trees

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Hash Maps/Sets
**Notes**

**Order Notation**

| Function   | Average O-Notation      | Worst O-Notation      |
|:----------:| -----------------------:| ---------------------:|
| insert     | O(1)                    | O(n)                  |
| erase      | O(1)                    | O(n)                  |
| find       | O(1)                    | O(n)                  |

**Space Complexity**
- Initial: O(1)
- Average: O(n)*

## Stacks
**Notes**
- LIFO: Last In First Out
- Could be implemented with a list or a vector/array
- By using a list, you could take advantage of the O(1) pop and push which is
frequently used with stacks.
- As elements come into the stack, the data structure can be imagined to be like
a stack of plates where the last, or most recently pushed element, is the first
element to be "popped" or removed off the stack.  Elements are always removed
in the reverse order that they were added, and elements cannot be accessed
randomly.
- You can think of computer memory while executing a program as utilizing a
stack.  For instance, when a function starts, a function pointer is added onto
"the stack" and let's say it calls another function.  That function's pointer
gets added onto the stack.  When it completes, the function pointer is "popped
off" and returned to the previous function.  Similarly, recursion would be
dependent on a stack like usage of memory as it must return to what previously
called the current iteration.

**Order Notation**

| Function   | Average O-Notation | Worst O-Notation |
|:----------:| ------------------:| ----------------:|
| push       | O(1)               | O(n)* or O(1)*   |
| pop        | O(1)               | O(n)* or O(1)*   |

\* Depends on whether you use a vector or a list

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Queues
**Notes**

**Order Notation**

| Function   | Average O-Notation | Worst O-Notation |
|:----------:| ------------------:| ----------------:|
| push       | O(1)               | O(n)* or O(1)*   |
| pop        | O(1)               | O(n)* or O(1)*   |

\* Depends on whether you use a vector or a list

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Heaps (Binary Heap | Min/Max)
**Notes**

**Order Notation**

| Function              | Average O-Notation     | Worst O-Notation |
|:---------------------:| ----------------------:| ----------------:|
| percolate_up          | O(log n)               | O(log n)         |
| percolate_down        | O(log n)               | O(log n)         |
| get_min/get_max       | O(1)                   | O(1)

**Space Complexity**
- Initial: O(1)
- Average: O(n)

## Priority Queue
**Notes**

**Order Notation**
- See Heaps

**Space Complexity**
- Initial: O(1)
- Average: O(n)
