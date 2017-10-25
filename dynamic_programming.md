# Dynamic Programming

breaking problems into subproblems that can be used to optimize solutions

reuse work you've already done!

##### Top-Down

* 'memoization'
* typical of recursive implementations that depend on solutions further down the chain
* build stacks and save the work to a cache as you bubble up

##### Button-Up

* iterative solutions

the fibonacci problem we've done uses two recursive calls, exponential time complexity

### Recursion

* a function that calls itself
* a relationship, function, or sequence is recursively defined if successive entries or outputs rely on previous entries/outputs

2 things to identify:
* base case
* recursive relationship

* a recursive relationship is a backwards chain that terminates at the base case

##### Making Change

you are given:
* a set of legal coins
* amount of change to make

you may need to:
* return minimum amount of coins needed to make change
* determine whether the amount is possible given the coins
* return all possible sets of coins that could make the change
* return the best possible set of coins (smallest number of coins)

##### When to use recursion?

* working backwards feels natural
  * if you can't visualize the whole thing, there should be some chain or decision tree in place
* the problem can be broken into smaller subproblems of the same type
* similar problems can be solved using recursion


### Recursive Time complexity

* evaluate time complexity of a single call to the function (excluding recursive calls)
* find the number of times the function is called (and with what inputs)
* add together the total time complexity from each individual call
  * if the function is constant, the total time complexity will be O(number of calls)

### Dynamic Programming

combines recursion with memoization to achieve faster runtimes while still utilizing the recursive relationships inherent in many computer science problems

two ways to approach dynamic programming:
* **Top-Down**: start at the top of the big call tree and record answers as you get them
* **Bottom-Up**: start at the bottom of the big call tree and record only the answers you know you'll need and return the answer you want once you have it

initialize a **cache** as a hash for easy lookup

we'll use this only for **top-down** implementations

for **bottom-up** implementations, a helper function will build up and return the cache

##### Examples:

**Blair Numbers**
* the first two are 1 and 2
* the kth blair number is the sum of the previous 2 blair numbers plus the (k - 1st) odd number
* return the nth blair number
