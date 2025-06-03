# 📊 Upper Confidence Bound (UCB) - Ad Selection Optimization

This project implements the **Upper Confidence Bound (UCB)** algorithm to solve the **Multi-Armed Bandit** problem using a real-world inspired dataset. The objective is to maximize ad click-through rates (CTR) by intelligently selecting ads over time based on exploration and exploitation strategies.

---

## 🧠 What is UCB?

UCB is a powerful reinforcement learning algorithm for decision-making problems where the agent must choose between multiple options (ads) and learn over time which ones perform best.

It strikes a balance between:
- 🔍 **Exploration**: Trying new or less frequently selected ads
- 💡 **Exploitation**: Choosing ads that have performed well in the past

---

## 📁 Files

- `ucb_ads.py` – Core script implementing the UCB algorithm
- `Ads_CTR_Optimisation.csv` – Dataset with simulated user clicks for 10 ads across 10,000 rounds

---

## 📈 Algorithm Overview

At each round:
1. For each ad, calculate an **upper confidence bound**.
2. Select the ad with the highest upper bound.
3. Update reward statistics and repeat.

Mathematically:
```python
upper_bound = average_reward + sqrt( (3/2) * log(n + 1) / number_of_selections )
