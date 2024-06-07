# Dikjstra algorith - short path

Find the shortest path to one vertice to all other vertices using vertices and edges, using an analogy to reality, the vertices are the cities and the edges are te roads that connect they \
Every vertice had some attributes:

-   Vertice
    -   List<\*edge> paths
    -   edge \*prev_path
    -   unsigned float best_distance
    -   bool explored

List paths is all the connections that vertice had \
prev_path is a path between this vertice and another, one from the List. Is used to rebuild the path, it's basicaly reverse-engineering because only build the short_path when reach the end-vertice \
prev_path is used to rebuild the shortest path between two vertices, when code reach the end-vertice \
best_distance is the distance between this vertice and the start-vertice, from default is infinite (in code will be 0) \
explored only tell if the code alredy have been here, if the vertice alredy explored \

Edges had another structure:

-   Edge
    -   Vertice *A, *B
    -   unsigned float distance

Vertice *A and *B store the vertices that edge connect \
unsigned distance is the distance between vertice A and B \

To find the shortest path, diskjtra use best_estimative logical

## Best_estimative

The best_estimative can be divided into two steps:

1. estimate the distance between actualy vertice and connected vertices, to every edge do:
    1. get actualy distance
    2. add with edge distance
    3. if distance is minor

Usually represented to find the path from start vertice to ALL others, but can be used to find between start and end vertices \

Find the path using the best_estimative logical, check the distances between actualy vertice and the vertices that exist a edge, a path between two vertices,

## References

<https://www.w3schools.com/dsa/dsa_algo_graphs_dijkstra.php> \
<https://youtu.be/EFg3u_E6eHU>
