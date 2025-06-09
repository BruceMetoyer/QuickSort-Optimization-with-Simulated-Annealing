# QuickSort-Optimization-with-Simulated-Annealing

An adaptive version of the QuickSort algorithm that uses **Simulated Annealing (SA)** to select near-optimal pivot elements at each recursive step. This project demonstrates how probabilistic optimization techniques can improve sorting efficiency by reducing comparisons, swaps, and partition imbalance.

## Overview

Traditional QuickSort performance heavily depends on the quality of pivot selection. This project introduces a novel pivot selection method using **Simulated Annealing**, which dynamically minimizes a custom cost function to select better pivots.

---

## Features

- Implements QuickSort with:
  - First, Last, Median, and Random pivot strategies
  - **Simulated Annealing-based pivot selection**
- Tracks and compares:
  - Swaps
  - Comparisons
  - Pivot selection cost
- Tested on multiple array types:
  - Sorted
  - Reverse-sorted
  - Random
  - Nearly sorted
  - Duplicate-heavy

---

## Experiment Setup

- Language: Python 3
- Tools: Jupyter Notebook, NumPy
- Metrics used:
  - `comparisons`, `swaps`, `partition imbalance`
- SA Parameters:
  - Initial Temp: `10`
  - Cooling Schedule: `T = initial_temp / (iteration + 1)`
  - Iterations per step: `100`

---

## Results Summary

- **SA-QuickSort** had the lowest overall cost across all test arrays
- Outperformed traditional strategies in comparisons and pivot balance
- Limitations:
  - Sensitive to parameter tuning
  - Overhead for small arrays
  - Weaker performance with duplicate-heavy arrays

---

## Future Work

- Integrate with neural networks for adaptive learning
- Explore hybrid models (e.g., SA + Genetic Algorithm)
- Improve duplicate handling and parallel performance

---

## 📁 Project Structure

SA-QuickSort/
│
├── sa_quicksort.py # Core SA-optimized QuickSort implementation
├── traditional_quicksort.py# Baseline pivot strategies (first, last, median, random)
├── cost_function.py # Custom cost metric for evaluating pivots
├── experiment_runner.ipynb # Full experimental setup and analysis
├── plots/ # Visual results and comparison graphs
├── README.md

## Acknowledgemmnets

Special thanks to Bowie State University's Computer Science Depeartment for providing me with the resources to accomplish this project.
