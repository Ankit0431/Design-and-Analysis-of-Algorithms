# Prim's Algorithm for Minimum Spanning Tree

## Overview

This repository contains an implementation of Prim's algorithm for finding the minimum spanning tree (MST) in a fully connected graph representing the telecommunications organization's offices located in different cities. The goal is to minimize the cost of connecting all offices using leased phone lines.

## Problem Definition

The telecommunications organization has offices spread across multiple locations globally and aims to minimize the cost of connecting all offices with leased phone lines. The problem involves constructing a fully connected graph representing the connections between offices and finding the minimum spanning tree to minimize the total cost.

## Input

- **City Locations**: Latitude and longitude coordinates of cities where offices are located.
- **Connection Costs**: Cost of connecting each pair of offices based on the distance between cities.

## Output

- **Minimum Spanning Tree**: A tree that connects all offices with minimum total cost, ensuring that every office is reachable from every other office with the least number of leased phone lines.

## Approach

1. **City Locations**:
   - Obtain latitude and longitude coordinates of cities in the same state using the geopy library.
   - Consider 4 to 6 cities for connecting offices.

2. **Connection Costs**:
   - Calculate the distance between each pair of offices (cities) using latitude and longitude coordinates.
   - Construct a fully connected graph with cities as nodes and distances as edge weights.

3. **Prim's Algorithm**:
   - Initialize an empty set of vertices and an empty set of edges.
   - Choose an arbitrary starting vertex.
   - Iterate until all vertices are included:
     - Select the edge with the minimum weight that connects a vertex in the set to a vertex outside the set.
     - Add the selected edge and vertex to the minimum spanning tree.
     - Update the set of vertices.

4. **Output**:
   - Return the minimum spanning tree, representing the optimal connections between offices.

## Real-life Use Cases

1. **Telecommunications Network Optimization**: Telecom companies use Prim's algorithm to optimize network connections between offices or cell towers, minimizing infrastructure costs while ensuring efficient communication.

2. **Transportation Planning**: Urban planners utilize Prim's algorithm to design efficient transportation networks, minimizing travel distances and infrastructure costs for connecting cities or neighborhoods.

3. **Power Grid Optimization**: Electric utilities apply Prim's algorithm to optimize power grid connections, minimizing transmission costs while ensuring reliable electricity supply to all regions.
