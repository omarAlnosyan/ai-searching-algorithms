
# **AI Search Optimization - Project 2024**

## 📌 **Introduction**
This project explores and compares three AI-based search algorithms: **Greedy Heuristic, Hill Climbing, and Beam Search**. A set of nodes is divided into clusters to maximize the objective function. The evaluation is based on the weights assigned to the nodes while maintaining the specified boundaries for each cluster. The nodes are connected in a graph structure with weighted edges.

## 🚀 **Algorithms Used**
1. **Greedy Heuristic**  
   - Selects the nodes with the largest weight and assigns them to clusters while respecting the total weight constraint.
   - Offers the fastest results but often sacrifices solution quality.  

2. **Hill Climbing**  
   - Starts with an initial solution from the Greedy Heuristic and improves it by swapping nodes between clusters.
   - Provides high-quality solutions but may take longer to converge.  

3. **Beam Search**  
   - Generates multiple solutions close to the current solution and selects the best one based on the objective value.
   - Balances between quality and speed but is computationally expensive.

## 🔧 **Initial Setup**
The project uses two files containing the **nodes, weights, and algorithm details**.  
In the pre-processing stage, the first line of each file is extracted to draw the graph and determine the nodes and weights
![image](https://github.com/user-attachments/assets/ca5c88f8-12a1-467d-8838-cc44735b5d64)
![image](https://github.com/user-attachments/assets/c3cf71b6-56a5-4f5e-9bed-d893d53b77c6)


## 🏗 **Implementation**
- A **Graph Class** is used to construct a graph representation with nodes, edges, and assigned weights.
- A **Solution Class** is implemented to generate clusters and compute the objective function.
- The algorithms (Greedy Heuristic, Hill Climbing, Beam Search) are applied to find optimal solutions
- ![image](https://github.com/user-attachments/assets/8ee4ca96-6c48-407f-8c44-b3a138688125)
- ![image](https://github.com/user-attachments/assets/f3c6bb58-5cc8-45b6-a0da-1d43f0045652)
- ![image](https://github.com/user-attachments/assets/e4ed8687-613f-4c7a-96e3-6f47280a842a)
- ![image](https://github.com/user-attachments/assets/f9661561-abe5-4da9-a495-e3e66627194e)

## 📊 **Results Summary**
The following results were obtained from two datasets: **Sparse82.txt (82 nodes)** and **RanReal480.txt (480 nodes).**

### **1. Sparse82.txt (82 Nodes)**
**Solution Quality:**
- **Hill Climbing** achieved the best objective value (**755.23**), significantly outperforming the other algorithms.
- **Beam Search** achieved a moderate value (**355.41**).
- **Greedy Heuristic** produced the lowest value (**151.55**).

**Execution Time:**
- **Greedy Heuristic** was the fastest (**0.00009 seconds**).
- **Hill Climbing** took slightly longer (**1.61 seconds**).
- **Beam Search** was the slowest (**8.12 seconds**).

---

### **2. RanReal480.txt (480 Nodes)**
**Solution Quality:**
- **Hill Climbing** achieved the best objective value (**423857.96**).
- **Beam Search** ranked second (**307657.04**).
- **Greedy Heuristic** produced the lowest value (**291870.97**).

**Execution Time:**
- **Greedy Heuristic** was significantly the fastest (**0.011 seconds**).
- **Hill Climbing** took much longer (**502.47 seconds**).
- **Beam Search** was extremely slow (**13534.00 seconds**).

---

### **Key Observations**
- **Hill Climbing** provides the best **solution quality**, but takes significantly more time.
- **Greedy Heuristic** is the **fastest** but produces lower-quality solutions.
- **Beam Search** offers a middle ground but becomes impractically slow for large datasets.

#### **Recommendations:**
- If the **solution quality** is the top priority → **Hill Climbing** is the best choice.
- If **execution time** is the critical factor → **Greedy Heuristic** offers fast solutions at the expense of quality.
- If a **balance** is needed → **Beam Search** is a suitable option, but only for smaller problems.

## 🛠 **How to Run the Code**
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/REPOSITORY_NAME.git
   ```
2. Install dependencies (if required):
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook source_code2.ipynb
   ```

---

