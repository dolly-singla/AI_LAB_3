# AI-LAB3-A-SEARCH
 What is A* Search?

A* (pronounced "A star") is a pathfinding and graph traversal algorithm widely used in Artificial Intelligence and Game Development.

It finds the shortest optimal path from a given source to a destination node.

A* uses a combination of:

G(n): The actual cost from the start node to the current node.

H(n): A heuristic estimate of the cost from the current node to the goal.

F(n) = G(n) + H(n): The total estimated cost of the path through n.

This makes A* both complete (it always finds a solution if one exists) and optimal (it guarantees the shortest path).

# About the Code

The grid/board is represented as a 2D list.

1 → traversable cell with cost = 1.

-1 → obstacle (not allowed).

The algorithm explores 8 possible moves (up, down, left, right, and diagonals).

A priority queue (heapq) is used to always expand the node with the lowest estimated cost.

The heuristic used is the Manhattan distance.

Output:

The optimal path from source to destination.

The cost of that path.

# Time Complexity

In the worst case, A* explores all nodes, so the complexity is:
O(E log V)

V = number of vertices (cells in the grid).

E = number of edges (possible moves between cells).

The log V factor comes from priority queue operations (heapq).

For a grid of size m × n:

V = m × n

Each node has up to 8 neighbors, so E ≈ 8 × V

Thus, O(m × n log(m × n))

# Space Complexity

The algorithm stores:

Open set (priority queue) → up to O(V) nodes.

Closed set → up to O(V) nodes.

Therefore, space complexity is O(V) = O(m × n).
