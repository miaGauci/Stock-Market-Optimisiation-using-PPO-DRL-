# Stock-Market-Optimisiation-using-PPO-DRL-

## 📘 Project Overview

This project investigates how **Deep Reinforcement Learning (DRL)** can be applied to identify **optimal investment strategies** in financial markets.  
It focuses on the **Proximal Policy Optimization (PPO)** algorithm — a leading DRL approach for continuous control — and compares its performance against traditional investment strategies.

The research explores how PPO agents trained on different neural architectures (**MLP**, **CNN**, and **RNN**) can make portfolio allocation decisions across a basket of **seven technology stocks**.  
Results show that DRL-based agents can **outperform passive investment benchmarks** such as the Buy-and-Hold strategy.

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

---
