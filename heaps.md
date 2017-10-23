# Heaps

priority queue; entries enter the back of the line

tiered system (bronze, silver, gold, platinum):
* items of the same order can take whatever order, but the priority levels
need to be ordered properly (B->S->G->P)

linked list not ideal for tiered priority queue

LRU Cache pretty good

----------------
**Heaps** (minimum or binary heap)

3 public methods: (besides initialize)
* peek: returns minimum priority item (smallest integer in data structure)
  * constant time
* insert: pushes element into the right place
  * add a node at bottom left-most spot and then correct
  * nodes will have to check their parents, make sure they're following the rules
* extract: removes element from data structure
  * when you take something out, you swap it with the bottom, right-most
  node, then correct with heaping up or down as needed

**a heap is a binary tree!**

always doubles the number of nodes at each level

complete trees: every node has children except possibly bottom row, and
no gaps
* must fill in from the left-most node

**a heap must be a complete tree, must obey heap property**

heap property: for each node, the parent must be less than or equal
* if they're not, they will swap

heapifying up and down:
nodes need to be able to figure out when one node shouldn't be the parent
of another

------------------------

Heaps are represented as arrays!
(because those methods would obviously be confusing to code)

no nesting; just each row, left-to-right

| parent | children |
|--------|--------|
| 0 | 1, 2 |
| 1 | 3, 4 |
| 2 | 5, 6 |
| 3 | 7, 8 |
| 4 | 9, 10 |

parent: 2idx + 1, 2idx + 2

child: (idx - 1) / 2

---------------------

**Heap Sort**

 max heap: parents must be larger, not smaller
 heapsort right to left, heapify down
