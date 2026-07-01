# Graph Visualizer

An interactive command-line tool for building graphs and watching classic graph algorithms — **BFS**, **DFS**, and **Dijkstra's shortest path** — execute step by step in real time.

Each traversal is rendered frame-by-frame in the terminal, showing the current node, the state of the queue/stack, visited nodes, and (for Dijkstra) live distance updates as edges are relaxed.

## Features

- **Build graphs interactively** — directed or undirected, weighted or unweighted
- **Breadth-First Search** — animated queue processing with visited-node highlighting
- **Depth-First Search** — animated stack processing (iterative, non-recursive)
- **Dijkstra's Algorithm** — live shortest-path distance table with edge relaxation events
- **Cycle detection** — checks whether the graph contains a cycle
- **Connectivity check** — verifies whether the graph is fully connected
- Colorized terminal output for readability

## Custom Data Structures

Core containers (`Queue`, `Stack`, `Vector`) used throughout the project are hand-implemented from scratch rather than pulled from the STL, living under [`external/stl-lite`](external/stl-lite). This was a deliberate choice to reinforce how these structures work under the hood before leaning on `std::` equivalents.

## Getting Started

### Prerequisites

- CMake 3.x or later
- A C++ compiler with C++17 support (GCC, Clang, or MSVC)

### Build

```bash
git clone https://github.com/<your-username>/graph-visualizer.git
cd graph-visualizer
mkdir build && cd build
cmake ..
cmake --build .
```

### Run

```bash
./graph_visualizer
```

## Usage

On launch, you'll get a menu:

```
=====================================
         GRAPH VISUALIZER
=====================================
1. Read Directed Graph
2. Read Undirected Graph
3. Print Graph
4. BFS
5. DFS
6. Dijkstra
7. Check Connectivity
8. Check Cycle
9. Exit
=====================================
```

1. Start by reading in a graph (option 1 or 2) — you'll be prompted for the number of vertices, each vertex's label, its neighbors, and (if weighted) edge weights.
2. Run any of the traversal or algorithm options to see it animate step by step.

## Project Structure

```
graph-visualizer/
├── include/            # Header files (Graph, algorithms, visualizer)
├── src/                # Implementation files
├── external/stl-lite/  # Custom Queue, Stack, and Vector implementations
└── CMakeLists.txt
```

## License

This project is available for personal and educational use.
