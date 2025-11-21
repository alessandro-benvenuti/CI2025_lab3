# Graph Pathfinding Algorithm Implementation and Benchmarking
This project implements, tests, and benchmarks various shortest path algorithms on custom-generated, weighted, and directed geometric graphs. It also focuses on the challenges posed by negative edge weights.

## Algorithms Overview

| Algorithm | Goal | Core Technique | Complexity |
|-----------|------|----------------|------------|
| **A* (`search`)** | Shortest Path (Non-Negative Weights) | Dijkstra + **Euclidean Heuristic** (h(n)) | O((V + E) log V) |
| **SLF/SPFA (`search_negative`)** | Shortest Path (Negative Weights) | Bellman-Ford optimization using a **Deque** and **SLF Heuristic** for queue ordering. | O(V · E) (Worst Case) |
| **Positive Simple Path (`search_only_positive_paths`)** | Shortest **Simple** Path with **Cost > 0** | **Backtracking Search** with pruning (Exponential complexity) | NP-Hard |

