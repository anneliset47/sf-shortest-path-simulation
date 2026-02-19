# San Francisco Shortest Path Simulation

Implementation of Dijkstra’s Algorithm to compute the fastest driving route between major San Francisco landmarks under normal and rush-hour traffic conditions.

## Project Overview

This project models route optimization using graph theory and shortest-path algorithms. 

We simulate travel between 10 major San Francisco landmarks and determine the fastest route from **Twin Peaks** to the **Golden Gate Bridge** using:

- Dijkstra’s Algorithm
- Priority Queues and Min-Heaps
- Weighted Graph Structures
- Stochastic Traffic Simulation

Two scenarios are analyzed:
1. Base Case (Average Traffic)
2. Rush Hour Traffic with Randomized Congestion Events

## Scenario 1: Base Case (Average Conditions)

- Driving times between landmarks were collected from Google Maps.
- The city map was represented as a weighted graph.
- Dijkstra’s Algorithm was used to compute the shortest travel time.

### Result

Shortest route:
A → D → I → J

Travel time: **20 minutes**

Manual calculations confirmed the algorithm’s result.

## Scenario 2: Rush Hour Simulation

To model realistic congestion:

- Traffic weights were modified using a **normal distribution** (mean = 2, SD = 0.5).
- A **20% probability high-impact event** was introduced.
- Edge weights were dynamically adjusted per simulation run.

### Example Result

Shortest route under traffic:
A → D → I → J

Travel time: **51 minutes**

Each simulation run produces different weights and outcomes.

## Technical Implementation

### Data Structures Used

- Dictionary-based graph representation
- Min-Heap (heapq)
- Priority Queue
- Sets for visited nodes

### Algorithm

Dijkstra’s Algorithm:

1. Initialize distances (source = 0, others = ∞)
2. Use priority queue to select smallest-distance node
3. Relax edges
4. Update distances
5. Repeat until all nodes are visited

## Key Concepts Demonstrated

- Graph modeling
- Shortest-path optimization
- Heap-based priority queues
- Stochastic simulation
- Manual algorithm validation
- Algorithm scalability analysis

## Future Improvements

- Return full path, not just travel time
- Add visualization of selected route
- Extend to larger graph datasets
- Compare with A* search algorithm






