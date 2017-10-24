# Binary Search Tree

data structures:
array
sorted array (improves time complexity for certain operations)
min/max heap (better still for time complexity)

#find method has O(n), O(log n), O(n) ...
#insert method has O(1), O(n), O(log n) ...
#delete method has O(n), O(n), O(log n) ...
... time complexity for each of these data structures, respectively

* log n, when n is very large, is almost constant

### we want BST to give us O(log n) time on all of these methods

* all BST nodes have at most 2 children
* every node in left subtree must be less than root node
* every node in right subtree must be greater than root node
* both subtrees are also binary search trees (recursion!)
* equality cases need to be defined and executed consistently
* if we find a dead end, return false, else, true

depth: number of levels
O(depth) is the #find time complexity

* if deleting a node with children, must choose a replacement node that follows the basic rules already set
* find the largest (right-most) node in the left subtree
  * any left child will replace it when it moves up
  * could also find the min on the right side
* hibbard deletion: a popular deletion algorithm

depth should equal log(n)

balanced binary search tree:
* difference in depth of left and right subtrees is not more than 1
* left and right subtrees are also balanced (recursive definition)

the insertion and deletion covered will run the risk of giving us a time complexity O(SQRT n)

#### self-balancing (AVL) trees

helps to have a method ::rebalance
