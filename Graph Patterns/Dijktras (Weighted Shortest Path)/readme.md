# Shortest Path / Dijkstra Patterns

## 1. Basic Dijkstra (Single Source Shortest Path)

**Core Idea:** Standard Dijkstra, distance accumulation.

* Network Delay Time (743)
* Reachable Nodes In Subdivided Graph (882)
* The Maze II (505)

## 2. Grid Dijkstra

**Core Idea:** Matrix treated as graph.

* Path With Minimum Effort (1631)
* Swim in Rising Water (778)
* Minimum Cost to Make at Least One Valid Path in a Grid (1368)

## 3. Counting Shortest Paths

**Core Idea:** Maintain both `dist[]` and `ways[]`.

* Number of Ways to Arrive at Destination (1976)
* Count Paths (CSES)
* Restricted Paths From First to Last Node (1786)

## 4. State Dijkstra

**Core Idea:** State = `(node, extra information)`.

* Cheapest Flights Within K Stops (787)
* Minimum Cost to Reach Destination in Time (1928)
* Shortest Path Visiting All Nodes (847)

## 5. Modified Relaxation Formula

**Core Idea:** Relaxation is NOT `dist[u] + wt`.

* Path With Minimum Effort (1631)
* Swim in Rising Water (778)
* Path With Maximum Probability (1514)

## 6. Multi-Source Shortest Path

**Core Idea:** Push many sources initially.

* 01 Matrix (542)
* As Far from Land as Possible (1162)
* Map of Highest Peak (1765)

## 7. K-th / Alternate Shortest Path

**Core Idea:** Keep more than one best distance.

* Find the K-th Smallest Sum of a Matrix With Sorted Rows (1439)
* Find K Pairs with Smallest Sums (373)
* Flight Routes (CSES)

## 8. 0-1 BFS

**Core Idea:** Edge weights only `0` or `1`.

* Minimum Obstacle Removal to Reach Corner (2290)
* Minimum Cost to Make at Least One Valid Path in a Grid (1368)
* Shortest Path in a Grid with Obstacles Elimination (1293)

## 9. Negative Weights (Bellman-Ford)

**Core Idea:** Dijkstra fails.

* Bellman-Ford Algorithm
* Wormholes (UVa 558)
* High Score (CSES)

## 10. All-Pairs Shortest Path

**Core Idea:** Floyd-Warshall.

* Find the City With the Smallest Number of Neighbors at a Threshold Distance (1334)
* Floyd Warshall Algorithm
* Shortest Routes II (CSES)

# Interview-Focused core problems (Maximum ROI)

Solve in order:

1. Network Delay Time (743)
2. Path With Minimum Effort (1631)
3. Swim in Rising Water (778)
4. Number of Ways to Arrive at Destination (1976)
5. Cheapest Flights Within K Stops (787)
6. Minimum Cost to Reach Destination in Time (1928)
7. Minimum Obstacle Removal to Reach Corner (2290)
8. Minimum Cost to Make at Least One Valid Path in a Grid (1368)
9. Path With Maximum Probability (1514)
10. 01 Matrix (542)
11. Find the City With the Smallest Number of Neighbors at a Threshold Distance (1334)
