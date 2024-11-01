# Dijkstra’s Algorithm in C
This project contains a C program that implements Dijkstra’s Algorithm to find the shortest path from a source vertex to all other vertices in a weighted graph. The program takes the number of vertices, edges, and their weights as input, and outputs the shortest distance from the source vertex to each vertex in the graph.

## Process
User Input:

The user is prompted to enter the number of vertices and edges in the graph.
The user then inputs the edges along with their weights, specifying the connection between vertices and the cost associated with that connection.
Dijkstra’s Algorithm Implementation:

The function dijkstra initializes distances from the source vertex to all other vertices as infinite, except for the source itself, which is set to zero.
It uses a priority queue (or a simple array in this case) to repeatedly extract the vertex with the minimum distance, updating the distances of its adjacent vertices based on the weights of the edges.
Output:

The program prints the shortest distance from the source vertex to each vertex in the graph.
### Example
Consider a graph with the following edges and weights:

(0, 1, 4)
(0, 2, 1)
(1, 2, 2)
(1, 3, 1)
(2, 3, 5)

**Input:**
Number of vertices: 4
Number of edges: 5
Edges and weights:
0 1 4
0 2 1
1 2 2
1 3 1
2 3 5
Source vertex: 0

**Output:**
Shortest distances from vertex 0:
Vertex 0: 0
Vertex 1: 3
Vertex 2: 1
Vertex 3: 4

## Complexity Analysis

###Time Complexity
Worst Case: (O(V^2)), where V is the number of vertices in the graph.
This is because, in the simplest implementation using an array, each vertex is checked against all others to find the minimum distance.

### Space Complexity
Space Complexity: (O(V)), where V is the number of vertices.
The program uses an array to store the shortest distances from the source vertex to all other vertices.
Assumptions
The program assumes the graph is connected and contains non-negative weights.
It does not handle negative weight cycles, as Dijkstra's Algorithm is not suitable for graphs with negative weights.
