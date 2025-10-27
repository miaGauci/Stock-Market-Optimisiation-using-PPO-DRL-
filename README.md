# Stock-Market-Optimisiation-using-PPO-DRL-

## 📘 Project Overview

The research explores how PPO agents trained on different neural architectures (**MLP**, **CNN**, and **RNN**) can make portfolio allocation decisions across **seven technology stocks**. Each Neural Network was also tested with different features to investigate which ones perform better with each model.Results show that DRL-based agents can **outperform passive investment benchmarks** such as the Buy-and-Hold strategy.

---

## 🎯 Objectives

- Implement and evaluate **Proximal Policy Optimization (PPO)** for portfolio management.  
- Compare **MLP**, **CNN**, and **RNN** neural architectures.  
- Benchmark PPO performance against:
  - **Buy-and-Hold** strategy.  
  - **Supervised learning MLP** baseline.  
- Evaluate through **Monte Carlo simulations** to analyze stability and risk–reward trade-offs.

---

## 💡 Key Findings

- **MLP with market features** achieved the **most stable and consistent returns** (~152%).  
- **CNN with price-only inputs** achieved the **highest single-run return** (265%) but with higher volatility.  
- **RNN models** struggled to retain temporal dependencies, leading to weaker performance.  
- PPO-based DRL agents demonstrated the ability to **learn profitable and adaptive trading strategies**.

## 🧠 Methodology

### 1. Data

- **Stocks used:** `AAPL`, `MSFT`, `NVDA`, `GOOGL`, `AMZN`, `TSLA`, `META`  
- **Source:** [Yahoo Finance](https://finance.yahoo.com/) via `yfinance` API  
- **Period:**
  - Training: *Jan 2020 – Jan 2023*  
  - Testing: *Jan 2023 – Jan 2024*  
- **Inputs:**
  - Normalized daily closing prices  
  - Market features: **EMA**, **RSI**, **MACD**, **Bollinger Bands**

### 2. Reinforcement Learning Framework

- Custom **trading environment** designed around an **actor–critic PPO** structure.  
- The agent observes the market state, allocates portfolio weights, and receives rewards based on **daily returns**.  
- **Key hyperparameters:**
  - Discount factor (γ): `0.9`  
  - GAE smoothing (λ): `0.95`  
  - Clipping threshold (ε): `0.2`

### 3. Neural Architectures

| Architecture | Strength | Notes |
|---------------|-----------|-------|
| **MLP** | Stable, consistent | Best overall with market features |
| **CNN** | High potential | Captures spatial patterns, risk of overfitting |
| **RNN** | Temporal awareness | Struggled with temporal dependencies |

### 4. Evaluation

- 200 **Monte Carlo rollouts** per model to assess variance and robustness.  
- Performance metrics:
  - Total return  
  - Stability  
  - Convergence rate  
  - Training duration  
- Visualized with violin plots, convergence curves, and median portfolio trajectories.

---

## 📊 Results Summary

| Model | Input | Avg. Return | Risk Profile | Comments |
|--------|--------|--------------|----------------|------------|
| **MLP** | Features | **152%** | Low | Most consistent performer |
| **CNN** | Prices | 265% (max) | High | Highest peak return, less stable |
| **RNN** | Features | < Buy-and-Hold | Low | Underperformed |
| **Buy & Hold** | – | 103% | Moderate | Passive benchmark |

---
