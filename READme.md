# Lab02 - Traveling Salesman Problem (TSP)

The **Traveling Salesman Problem (TSP)** is a classic optimization problem in computer science and operations research. It aims to find the shortest possible route that visits each location in a set exactly once.

- **Number of Steps**: Equals the number of cities.

### More Information
For more details on the Traveling Salesman Problem, see this [article on Routific](https://www.routific.com/blog/travelling-salesman-problem#:~:text=The%20Travelling%20Salesman%20Problem%20(TSP,set%20of%20locations%20just%20once).

---

## Solution Approaches

### 1. Greedy Nearest-Neighbor Approach
- The `tsp_greedy` function solves TSP by following a **greedy, nearest-neighbor strategy**. Starting from the first city (index 0), it repeatedly selects the closest unvisited city, visiting all cities one by one.
- Once all cities have been visited, the function returns to the starting city to complete the round trip. This ensures that the total travel distance is minimized as much as possible by the greedy algorithm.
- **Execution Time**: Approximately 1 minute.

### 2. Simulated Annealing
- The `simulated_annealing` function implements the **Simulated Annealing** algorithm to solve TSP. It begins with a random path and iteratively explores potential solutions by making slight modifications to the current path.
- If a new path has a shorter distance, it is accepted. Otherwise, it is accepted with a probability that decreases as the temperature decreases.
- The algorithm gradually lowers the temperature, reducing the chance of accepting worse solutions, which helps it converge to a near-optimal solution.
- The function ultimately returns the best path and the minimum distance found.
- **Execution Time**: Approximately 3 minute.

---

## Results

| File         | Simulated Annealing Distance (km) | Greedy Nearest-Neighbor Distance (km) |
|--------------|-----------------------------------|---------------------------------------|
| china.csv    | 62,496.74                         | 63,962.92                             |
| italy.csv    | 4,174.94                          | 4,436.03                              |
| russia.csv   | 40,665.66                         | 42,334.16                             |
| us.csv       | 34,037.59                         | 48,050.03                             |
| vanuatu.csv  | 1,345.54                          | 1,475.53                              |

---

This table shows that the Simulated Annealing approach generally produces shorter routes compared to the Greedy Nearest-Neighbor method, demonstrating its effectiveness in approximating a better solution for TSP.
