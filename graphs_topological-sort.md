# Graphs

* vertices (dots that represent the information)
* edges (lines that represent connection or relationship between dots)

* if the graph is directed, all edges need to be directed
* if the graph has weight, all edges need to be weighted

* example: Facebook
  * vertices: users
  * edges: friendships

|V| = number of vertices
|E| = number of edges

density = |E| / (|V| (|V| - 1))
(max density for undirected graph: 1)
(min density: 0 -- entirely disconnected graph)

(max density changes for directed (vs undirected) graphs: 2)

* example: Twitter
  * vertices: users
  * two different types of relationships with Twitter
    * follows are only one-way
    * need a directed graph

a tree is a type of connected graph
* n vertices
* n - 1 edges

a tree example: the DOM
* vertices: DOMElements
* edges: parents, children

tree density: 1 / |V|

dependency set: data that depends on other data

example: vertices are tasks; edges communicate where one task must be done before another
(must buy cat food before you feed your cat)

cycle: a path within a graph that starts and ends at the same vertex

adjacency matrix

# Topological Sort

if i must do task A before task B, there will be a directional edge between the two tasks, in a dependency set

Topological sort puts a dependency set in an appropriate order

* do all tasks that aren't dependent on anything first
  * cut out that vertex and all edges emanating therefrom
* next do all other tasks that don't have in-edges
* next do any tasks that emanate from the previous layer
* repeat
* order within layers does not matter

Kahn's Algorithm: (above)
* create a queue
* push in vertices with no in-edges
* pop off vertices from queue
* remove from graph (along with out-edges)
* push vertex into sorted array
* examine destination vertices, push onto queue if more in-edges

* vertex and graph classes needs access to edges



Final Notes:
* NOT deterministic (not a problem, unless it is)
* Coffman-Graham: another algorithm that IS deterministic
* modifying depth first search

Use cases:
* task/dependency list
* Webpack (because it creates a list of files with dependencies)
* schedule tasks/scheduling restrictions
* minimal spanning tree (eliminates redundancies when traversing a tree)
