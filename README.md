# 🍳 Cloud Kitchen Decision Engine & Optimization Pipeline

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Optimization](https://img.shields.io/badge/Optimization-MILP%20%7C%20PuLP-green.svg)](https://coin-or.github.io/PuLP/)
[![Game Theory](https://img.shields.io/badge/Game%20Theory-Shapley%20%7C%20Nash-orange.svg)](https://en.wikipedia.org/wiki/Game_theory)

An advanced, data-driven decision engine designed to optimize the operations, synergy, and logistics of a shared cloud kitchen complex. By combining statistical data analysis, mathematical optimization, algorithmic game theory, and stochastic simulation, this project models and solves complex resource-allocation and strategic-pricing challenges.

---

## 🚀 Key Features & Architecture

The project is structured into four main computational phases, translating raw historical demand data into optimized, synergistic business strategies:

### 📊 1. Exploratory Data Analysis & Individual Optimization
* **Demand Profiling:** Conducted statistical analysis (Coefficient of Variation - CV) on historical demand data to classify stability across different kitchens ("Beshroni", "Via Italy", "Yaroka").
* **Local MILP Models:** Formulated and solved Mixed-Integer Linear Programming (MILP) models using `PuLP` to maximize daily individual profits under strict raw material and capacity constraints.

### 🤝 2. Cooperative Game Theory & Synergy Optimization
* **Global Coalition MILP:** Modeled a unified mathematical optimization problem where kitchens share raw materials and cooking capacities to achieve a global optimum.
* **Shapley Value Allocation:** Used cooperative game theory to fairly distribute the coalition's synergistic bonus (totaling ₪180) based on each kitchen's marginal contribution.

### ⚖️ 3. Non-Cooperative Game Theory (Strategic Pricing)
* **Strategic Pricing Grid:** Constructed a $3 \times 3 \times 3$ payoff matrix representing high, medium, and low pricing strategies for all kitchens.
* **Nash Equilibrium:** Implemented an algorithmic solver to identify pure-strategy Nash Equilibria, determining stable market pricing points.

### 🚚 4. Stochastic Queuing Logistics & Pigouvian Tax
* **Queuing Simulation:** Modeled the delivery dispatch network as an $M/E_2/5$ queuing system (Markovian arrivals, Erlang-2 service times, 5 delivery couriers) to compute critical KPIs like average waiting time and queue length.
* **Pigouvian Congestion Tax:** Designed a dynamic taxation mechanism applied during peak hours to internalize negative externalities (delivery delays) and optimize system-wide social welfare[cite: 1].

---

## 🛠️ Tech Stack & Libraries

* **Language:** Python 3.8+
* **Mathematical Optimization:** `PuLP` (COIN-OR CBC Solver)
* **Data Science & Analytics:** `pandas`, `numpy`, `scipy`
* **Visualization:** `matplotlib`

---

## ⚙️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/cloud-kitchen-decision-engine.git](https://github.com/YOUR_USERNAME/cloud-kitchen-decision-engine.git)
   cd cloud-kitchen-decision-engine
