# Delivery Route Optimization for E-commerce

**Capstone Assignment:** Algorithmic Strategies for Logistics  
**Course:** Data Structures and Algorithms  

---

## 📋 Project Overview

This project implements a comprehensive delivery route optimization system for e-commerce logistics, integrating multiple algorithmic paradigms:

- **Unit 1:** Recurrence Relations
- **Unit 2:** Greedy Algorithms & Dynamic Programming
- **Unit 3:** Graph Algorithms (Dijkstra, Prim's MST)
- **Unit 4:** Traveling Salesman Problem (TSP)

## 🎯 Problem Statement

Design an optimized delivery route for a vehicle starting from a warehouse, visiting customer locations to deliver parcels, while:
- Minimizing total travel time/distance
- Respecting delivery time windows
- Maximizing parcel value within capacity constraints

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. Clone the repository:
```
git clone <your-repo-url>
cd delivery_route_optimization
```

2. Install dependencies:
```
pip install -r requirements.txt
```

3. Run the Jupyter notebook:
```
jupyter notebook delivery_route_optimization.ipynb
```

---

## 📂 Project Structure

```
delivery_route_optimization/
├── delivery_route_optimization.ipynb    # Main notebook with all code
├── README.md                            # This file
├── requirements.txt                     # Python dependencies
└── images/                              # Generated visualizations
    ├── tsp_complexity_analysis.png
    ├── optimal_route_network.png
    └── parcel_analysis.png
```

---

## 🧮 Algorithms Implemented

### 1. Recurrence-Based Route Cost Estimation
- **Purpose:** Estimate total delivery cost recursively
- **Complexity:** O(n!)
- **Use Case:** Small instances for exact cost calculation

### 2. Greedy Parcel Selection
- **Strategy:** Select parcels by value/weight ratio
- **Complexity:** O(n log n)
- **Use Case:** Quick parcel prioritization within capacity constraints

### 3. Dynamic Programming for Time Windows
- **Purpose:** Validate delivery feasibility within time constraints
- **Complexity:** O(n! × n)
- **Use Case:** Ensure all deliveries meet time window requirements

### 4. Dijkstra's Shortest Path
- **Purpose:** Find shortest paths from warehouse to all customers
- **Complexity:** O(n²)
- **Use Case:** Individual route distance estimation

### 5. Prim's Minimum Spanning Tree
- **Purpose:** Connect all locations with minimum total distance
- **Complexity:** O(n²)
- **Use Case:** Network connectivity analysis

### 6. TSP - Brute Force
- **Strategy:** Try all permutations
- **Complexity:** O(n!)
- **Use Case:** Small instances (n < 10) for optimal solution

### 7. TSP - Held-Karp Dynamic Programming
- **Strategy:** Memoization-based optimization
- **Complexity:** O(n² × 2ⁿ)
- **Use Case:** Medium instances (n < 15) for optimal solution

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| **Optimal Route** | Warehouse → C1 → C5 → C4 → C2 → C3 → Warehouse |
| **Total Distance** | 30 units |
| **Greedy Selection Value** | $165 |
| **Vehicle Utilization** | 96% (48kg / 50kg) |
| **MST Cost** | 21 units |

---

## 📈 Visualizations

### 1. TSP Complexity Analysis
Shows exponential growth of computation time and factorial increase in permutations.

### 2. Optimal Route Network
Network graph visualization showing the optimal delivery route with distances.

### 3. Parcel Selection Analysis
Value vs. weight scatter plot and value/weight ratio bar chart showing greedy selection criteria.

---

## 💡 Insights & Analysis

### Trade-offs: Optimality vs Computation Time

**Exact Algorithms (TSP):**
- ✅ Guarantee optimal solution
- ❌ Exponential time complexity
- ⚠️ Only feasible for small instances (n < 15)

**Approximation Algorithms (Greedy):**
- ✅ Polynomial time complexity
- ✅ Fast execution (milliseconds)
- ❌ No optimality guarantee
- ⚠️ May miss constraints (time windows)

### Real-World Recommendations

1. **Small routes (< 15 stops):** Use exact TSP with DP
2. **Medium routes (15-50 stops):** Use heuristics (2-opt, nearest neighbor)
3. **Large routes (> 50 stops):** Use route clustering + local optimization
4. **Always validate:** Use DP to check time window feasibility

---

## 🔬 Profiling Results

Execution time scaling for TSP:

| Customers | Permutations | Brute Force Time | DP Time |
|-----------|--------------|------------------|---------|
| 3 | 6 | < 0.001s | < 0.001s |
| 5 | 120 | < 0.001s | < 0.001s |
| 7 | 5,040 | < 0.001s | < 0.001s |
| 10 | 3,628,800 | ~seconds | ~seconds |
| 20 | 2.4 × 10¹⁸ | infeasible | infeasible |

---

## 🛠️ Technologies Used

- **Python 3.x**
- **NumPy** - Numerical computations
- **Matplotlib** - Visualizations
- **NetworkX** - Graph algorithms and visualization
- **Jupyter Notebook** - Interactive development

---

## 👨‍💻 How to Run Each Strategy

### Run Greedy Parcel Selection
```
selected, value, weight = greedy_parcel_selection(parcels, vehicle_capacity)
```

### Run TSP Optimization
```
route, cost = tsp_brute_force(locations, distance_matrix)
```

### Validate Time Windows
```
is_valid, schedule = validate_time_windows_v2(customers, parcels, distance_matrix, locations)
```

### Run Dijkstra's Algorithm
```
distances, predecessors = dijkstra_shortest_path(distance_matrix, 0)
```

---

## 📝 What Each Output Shows

- **Greedy Selection Output:** List of selected customers, total value, weight utilization
- **TSP Output:** Optimal route sequence, total distance, computation time
- **Time Window Validation:** Boolean feasibility, delivery schedule with arrival times
- **Dijkstra Output:** Shortest distances from warehouse to each customer
- **Visualizations:** Complexity growth, route network, parcel selection analysis

---

## 🎓 Learning Outcomes

✅ Modeled complex optimization as combination of algorithmic paradigms  
✅ Implemented recurrence, greedy, and DP strategies  
✅ Used graph algorithms for route building  
✅ Analyzed TSP intractability with empirical profiling  
✅ Created informative visualizations of results  

---

## 📧 Contact

**Student Name:** Chirag Yadav  
**Roll Number:** 2301201085  
**Course:** Data Structures and Algorithms  
**Semester:** 5  

---

## 📄 License

This project is submitted as academic coursework.

---

**Last Updated:** November 2025
