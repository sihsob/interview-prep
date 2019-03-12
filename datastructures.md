# Comprehensive Data Structures Review
This document will go over general important information about the listed data
structures including some "interview-like" formatted questions with responses.
Coding samples will be included separately.

## Arrays
**Features**
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

Pros:

Cons:

## Vectors
**Features**
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
Features:

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

Pros:

Cons:

## Trees
Features:

**Order Notation**

| Function   | Average O-Notation      | Worst O-Notation      |
|:----------:| -----------------------:| ---------------------:|
| insert     | O(log n)                | O(log n)              |
| erase      | O(log n)                | O(log n)              |
| find       | O(log n)                | O(log n)              |

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:

## Maps
Features:

**Order Notation**
- See Trees

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:

## Sets
Features:

**Order Notation**
- See Trees

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:

## Hash Maps/Sets
Features:

**Order Notation**

| Function   | Average O-Notation      | Worst O-Notation      |
|:----------:| -----------------------:| ---------------------:|
| insert     | O(1)                    | O(n)                  |
| erase      | O(1)                    | O(n)                  |
| find       | O(1)                    | O(n)                  |

**Space Complexity**
- Initial: O(1)
- Average: O(n)*

Pros:

Cons:

## Stacks
Features:

**Order Notation**

| Function   | Average O-Notation | Worst O-Notation |
|:----------:| ------------------:| ----------------:|
| push       | O(1)               | O(n)* or O(1)*   |
| pop        | O(1)               | O(n)* or O(1)*   |

/* Depends on whether you use a vector or a list

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:

## Queues
Features:
**Order Notation**

| Function   | Average O-Notation | Worst O-Notation |
|:----------:| ------------------:| ----------------:|
| push       | O(1)               | O(n)* or O(1)*   |
| pop        | O(1)               | O(n)* or O(1)*   |

/* Depends on whether you use a vector or a list

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:

## Heaps (Binary Heap | Min/Max)
Features:

**Order Notation**

| Function              | Average O-Notation     | Worst O-Notation |
|:---------------------:| ----------------------:| ----------------:|
| percolate_up          | O(log n)               | O(log n)         |
| percolate_down        | O(log n)               | O(log n)         |
| get_min/get_max       | O(1)                   | O(1)

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:

## Priority Queue
Features:

**Order Notation**
- See Heaps

**Space Complexity**
- Initial: O(1)
- Average: O(n)

Pros:

Cons:
