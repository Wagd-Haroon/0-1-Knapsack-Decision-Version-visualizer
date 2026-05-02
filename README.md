# 0-1-Knapsack-Decision-Version-visualizer
# 0/1 Knapsack Decision Version — Interactive Visualizer

An interactive web-based teaching tool for the **0/1 Knapsack Decision Problem**, 
built for BCS 309 — Algorithms I (Spring 2026) at the Canadian University Dubai.

🔗 **Live Tool:** https://wagd-haroon.github.io/0-1-Knapsack-Decision-Version-visualizer/

---

## What This Tool Covers

The 0/1 Knapsack Decision Problem asks: given *n* items with weights and values, 
a capacity *W* and a target value *V* — does any subset exist with total weight ≤ W 
and total value ≥ V? This YES/NO question is NP-complete.

The tool demonstrates three algorithms side by side, proves NP-completeness formally, 
and lets you step through every decision the algorithm makes in real time.

---

## Features

### 🔬 Visualizer Tab
- Step-by-step animation of **Dynamic Programming**, **Brute Force**, and **Greedy Heuristic**
- Full DP table visualization — each cell highlights as it is computed
- Traceback path lights up to show which items were selected
- Pseudocode panel with **live line highlighting** at every step
- Step-by-step log with plain-language explanations of each decision
- Custom item builder — add, delete, rename, and adjust weights/values freely
- 6 presets: YES Instance, NO Instance, Classic DP, Greedy Fails, Subset Sum, Tight Fit
- Speed slider, Step / Play / Pause / Reset controls
- Live statistics: operations count, cells visited, best value, decision

### 📖 Learn Tab
- Full problem definition (formal input/output/decision framing)
- DP state definition, recurrence, base cases, and inductive correctness proof
- Traceback algorithm with worked example
- Time and space complexity analysis (O(nW) pseudo-polynomial explained)
- Greedy counterexample: why value/weight ratio fails for 0/1 knapsack
- Key concept boxes: P, NP, NP-Complete, Certificate, Verifier, Pseudo-Polynomial

### 🔐 NP-Completeness Tab
Full formal proof that 0/1 Knapsack (Decision) is NP-complete, structured in 6 steps:
1. Problem statement with worked instance
2. NP membership — certificate (subset of indices) + O(n) verifier
3. Reduction from Subset Sum — construction: wᵢ = vᵢ = aᵢ, W = V = t
4. Correctness in both directions — forward and backward with numeric verification
5. Polynomial-time construction — O(n) derivation
6. Why DP (pseudo-polynomial O(nW)) does not contradict NP-completeness

### ⚖️ Comparison Tab
- Run all three algorithms on the same input simultaneously
- Side-by-side results, operation counts, and correctness indicators
- Highlights greedy suboptimality gap when it occurs
- Growth curve chart (log scale) — Brute Force vs DP vs Greedy

### 📊 Benchmark Tab
- Adjustable max *n* and capacity *W*
- Operation count table for each algorithm at each *n*
- Logarithmic growth chart showing how quickly Brute Force explodes vs DP and Greedy
- Practical guidance on which algorithm to use and when

---

## Algorithms Implemented

| Algorithm | Complexity | Exact? |
|---|---|---|
| Brute Force (bitmask) | O(n · 2ⁿ) | ✅ Yes |
| Dynamic Programming (bottom-up) | O(nW) pseudo-polynomial | ✅ Yes |
| Greedy (value/weight ratio) | O(n log n) | ⚠️ Heuristic |

---

## Technology

Built as a **single HTML file** — no frameworks, no external libraries, no dependencies.  
Pure HTML5, CSS3, and Vanilla JavaScript (ES6+).

