# 🚀 Topological Sort DSA Mastery Checklist

A curated collection of LeetCode problems mapped directly to the four core sub-patterns of the Topological Sort algorithm. Use this to systematic track your mastery over every variation of graph dependencies.

---

## 🧭 Sub-Pattern Progress Tracker

### 🛑 Pattern 1: Cycle Detection (Directed Graphs)
*Goal: Identify if a circular dependency exists or isolate the nodes/edges causing a structural deadlock.*

| Status | Problem | Difficulty | Link |
| :---: | :--- | :---: | :--- |
| [ ] | Loud and Rich | 🟡 Medium | [LeetCode 851](https://leetcode.com/problems/loud-and-rich/) |
| [ ] | Redundant Connection II | 🔴 Hard | [LeetCode 685](https://leetcode.com/problems/redundant-connection-ii/) |
| [ ] | Is Graph Bipartite? | 🟡 Medium | [LeetCode 785](https://leetcode.com/problems/is-graph-bipartite/) |
| [ ] | Minimum Fuel Cost to Report to the Capital | 🟡 Medium | [LeetCode 2477](https://leetcode.com/problems/minimum-fuel-cost-to-report-to-the-capital/) |
| [ ] | Check If a String Is a Valid Sequence from Root to Leaves | 🟡 Medium | [LeetCode 1430](https://leetcode.com/problems/check-if-a-string-is-a-valid-sequence-from-root-to-leaves-path-in-a-binary-tree/) |

---

### 🗺️ Pattern 2: Finding a Valid Ordering (Standard / Multi-Level)
*Goal: Construct a complete linear sequence where all multi-level prerequisite constraints are satisfied.*

| Status | Problem | Difficulty | Link |
| :---: | :--- | :---: | :--- |
| [ ] | Sort Items by Groups Respecting Dependencies | 🔴 Hard | [LeetCode 1203](https://leetcode.com/problems/sort-items-by-groups-respecting-dependencies/) |
| [ ] | All Ancestors of a Node in a Directed Acyclic Graph | 🟡 Medium | [LeetCode 2192](https://leetcode.com/problems/all-ancestors-of-a-node-in-a-directed-acyclic-graph/) |
| [ ] | Reconstruct Itinerary | 🔴 Hard | [LeetCode 332](https://leetcode.com/problems/reconstruct-itinerary/) |
| [ ] | Sequence Reconstruction | 🟡 Medium | [LeetCode 444](https://leetcode.com/problems/sequence-reconstruction/) |
| [ ] | Find All Possible Recipes from Given Supplies | 🟡 Medium | [LeetCode 2115](https://leetcode.com/problems/find-all-possible-recipes-from-given-supplies/) |

---

### ⚖️ Pattern 3: Lexicographically Smallest / Constrained Ordering
*Goal: Integrate a Priority Queue (Heap) instead of a standard Queue within Kahn's algorithm to satisfy a secondary sorting rule.*

| Status | Problem | Difficulty | Link |
| :---: | :--- | :---: | :--- |
| [ ] | Smallest String With Swaps | 🟡 Medium | [LeetCode 1202](https://leetcode.com/problems/smallest-string-with-swaps/) |
| [ ] | Minimize Malware Spread II | 🔴 Hard | [LeetCode 928](https://leetcode.com/problems/minimize-malware-spread-ii/) |
| [ ] | Rearrange String k Distance Apart | 🔴 Hard | [LeetCode 358](https://leetcode.com/problems/rearrange-string-k-distance-apart/) |
| [ ] | Single-Threaded CPU | 🟡 Medium | [LeetCode 1834](https://leetcode.com/problems/single-threaded-cpu/) |
| [ ] | Task Scheduler | 🟡 Medium | [LeetCode 621](https://leetcode.com/problems/task-scheduler/) |

---

### 📈 Pattern 4: Shortest / Longest Paths on a DAG (Graph DP)
*Goal: Process nodes in topological order to compute paths, minimum schedules, or cumulative values in $O(V + E)$ time.*

| Status | Problem | Difficulty | Link |
| :---: | :--- | :---: | :--- |
| [ ] | Parallel Courses | 🟡 Medium | [LeetCode 1136](https://leetcode.com/problems/parallel-courses/) |
| [ ] | Longest Increasing Path in a Matrix | 🔴 Hard | [LeetCode 329](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/) |
| [ ] | Maximum Path Quality of a Graph | 🔴 Hard | [LeetCode 2065](https://leetcode.com/problems/maximum-path-quality-of-a-graph/) |
| [ ] | Largest Color Value in a Directed Graph | 🔴 Hard | [LeetCode 1857](https://leetcode.com/problems/largest-color-value-in-a-directed-graph/) |
| [ ] | Minimum Time to Collect All Apples in a Tree | 🟡 Medium | [LeetCode 1443](https://leetcode.com/problems/minimum-time-to-collect-all-apples-in-a-tree/) |

---

## 🛠️ Implementation Cheat Sheet

### Kahn's Algorithm (BFS Template)
```python
def topological_sort(vertices, edges):
    indegree = {i: 0 for i in range(vertices)}
    graph = {i: [] for i in range(vertices)}
    
    # 1. Build Graph & Fill Indegrees
    for parent, child in edges:
        graph[parent].append(child)
        indegree[child] += 1
        
    # 2. Find all sources (indegree == 0)
    # Note: Swap out standard deque for a heapq (Min-Heap) for Pattern 3
    queue = deque([node for node in indegree if indegree[node] == 0])
    topo_order = []
    
    # 3. Process
    while queue:
        node = queue.popleft()
        topo_order.append(node)
        
        for neighbor in graph[node]:
            indegree[neighbor] -= 1
            if indegree[neighbor] == 0:
                queue.append(neighbor)
                
    # 4. If topo_order length != vertices, a cycle exists!
    return topo_order if len(topo_order) == vertices else []