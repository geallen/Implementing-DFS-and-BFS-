# Implementing-DFS-and-BFS-
Implementing Depth First Search and Bread First Search

This code is solution of below question.

Implementing the depth-first and breadth-first search algorithms. Your output should look similar to this:

*** Depth-First Search algorithm from a to g ***

Explored node Node(A, 0)

Frontier: [Node(B, 10), Node(D, 15)]

Explored node Node(D, 15)

Frontier: [Node(B, 10), Node(E, 55)]

Explored node Node(E, 55)

Frontier: [Node(B, 10), Node(C, 125), Node(F, 195)]

Explored node Node(F, 195)

Frontier: [Node(B, 10), Node(C, 125), Node(G, 215)]

-----> Solution: A -> D -> E -> F -> G (path_cost=215)



*** Breadth-First Search algorithm from a to g ***

Explored node Node(A, 0)

Frontier: deque([Node(B, 10), Node(D, 15)])

Explored node Node(B, 10)

Frontier: deque([Node(D, 15), Node(C, 130)])

Explored node Node(D, 15)

Frontier: deque([Node(C, 130), Node(E, 55)])

Explored node Node(C, 130)

Frontier: deque([Node(E, 55), Node(G, 140)])

Explored node Node(E, 55)

Frontier: deque([Node(G, 140), Node(F, 195)])

-----> Solution: A -> B -> C -> G (path_cost=140)


After showing the result of these two runs, add a link between states a and f with cost 50, then run the depth-first-search again.
New result should look similar to this:

-------- A new link between a and f is added ----------

Explored node Node(A, 0)

Frontier: [Node(B, 10), Node(D, 15), Node(F, 50)]

Explored node Node(F, 50)

Frontier: [Node(B, 10), Node(D, 15), Node(E, 190), Node(G, 70)]

-----> Solution: A -> F -> G (path_cost=70)


The path costs are shown in the output, but please note that they do not affect the decisions of breadth-first and depth-first search. You should take into account the priority rules of these two algorithms, while popping or pushing an item.

While expanding the nodes, child nodes are formed in alphabetical order. E.g. If there are two links from node a, one to b and the other to d, then link a-b is expanded first and b is placed in the frontier first.  When selecting the nodes from frontier, however, the order depends on the algorithm. Depth first search uses a LIFO queue (a stack). With the same example, since child node d is formed after node b, node d is selected first to be taken from frontier. On the other hand, breadth-first search uses a FIFO queue, so gives priority to explore node b before node d.
