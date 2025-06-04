# 🧭 Delivery Route Optimization — TSP Heuristics (NN & ACO)

This project explores delivery route optimization using the **Travelling Salesman Problem (TSP)** as a base model. It compares the performance of two basic heuristics — **Nearest Neighbor (NN)** and **Ant Colony Optimization (ACO)** — on a small subset of TSP instances. A particular focus is placed on the **total path cost** and the effect of **parameter tuning** on algorithm efficiency.

## 🚀 Objectives

- Model delivery scenarios as TSP instances.
- Implement two heuristics: Nearest Neighbor and ACO.
- Use **Optuna** to optimize ACO parameters.
- Compare results across several instances from the [TSPLIB dataset](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/).
- Visualize performance in terms of total distance/cost.

## 🛠️ Approach

- A small subset (10 instances) was selected from a public TSP dataset.
- For each instance, the distance matrix is used to evaluate:
  - A greedy **Nearest Neighbor** solution.
  - A default **ACO** solution.
  - An **ACO solution with parameters optimized** via **Optuna**.
- Key ACO parameters optimized:
  - `rho` (evaporation rate)
  - `alpha`, `beta` (pheromone influence vs heuristic)
  - Initial pheromone levels

## 📊 Visualization

The results are displayed as a grouped bar chart comparing the total path cost for each algorithm across different instance sizes.

## 📂 Project Structure
```
├── docs/     #Website for the Visualisation of Ant Colony Optimisation
├── poster/
│ └── DL_Poster.pdf
├── report/
│ └── DL_Rapport.docx
├── src/
│ └── deep-learning-mini-project.ipynb
├── results/
├── README.md
```

## 🧪 Installation & Usage

### 1. Clone the repository

```bash
git clone https://github.com/badrafyf77/Deep_learning_Mini_Project.git
cd Deep_learning_Mini_Project
```

### 2. Run the main script
```
python src/deep-learning-mini-project.ipynb
```
This will load the dataset, run all heuristics, optimize ACO parameters, and generate the comparison plot.

📚 References
TSPLIB: http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/

Dorigo, M., & Birattari, M. (2004). Ant Colony Optimization. Encyclopedia of Optimization.

Le Mercier, A. Solving the TSP with ACO [Kaggle Notebook].

Optuna: Akiba, T., et al. (2019). Optuna: A Next-generation Hyperparameter Optimization Framework.

📄 License
This project is released under the MIT License.

Authors: AFYF Badreddine, CHABBAKI Ayman, AYAR Hanane

Inspired by: Alexandre Le Mercier, Marco Dorigo, Mauro Birattari
