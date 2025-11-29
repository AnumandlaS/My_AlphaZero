# AlphaZeroFromScratch

The first time I have heard about systems like AlphaZero, DeepBlue, AlphaGo I was really interested to learn the brain behind them. So, this is just a very very small scale implementation of **AlphaZero from scratch** using PyTorch and Jupyter Notebooks, featuring self-play, Monte Carlo Tree Search (MCTS), and neural network training - applied to games like Tic-Tac-Toe and Connect Four.

---
Go has more possible board positions (around **10¹⁷⁰**) than the estimated number of atoms in the observable universe (**~10⁸⁰**), which shows just how unimaginably complex the game is. 😶😮😲🤯😱
---
## 📌 Overview

This repository implements the AlphaZero algorithm end-to-end with a strong focus on clarity, learning, and experimentation rather than heavy system optimization.

It includes:
- Monte Carlo Tree Search (MCTS)
- A neural network with policy and value heads
- Self-play data generation
- Model training loop
- Evaluation pipeline
- Game implementations (Tic-Tac-Toe, Connect Four)
- Pretrained models for quick testing

This project is ideal for learners who want a **deep understanding** of how AlphaZero works internally.

---

## 📂 Repository Structure

| Notebook / File | Description |
|----------------|-------------|
| `1.TicTacToe.ipynb` | AlphaZero pipeline applied to Tic-Tac-Toe |
| `2.MCTS.ipynb` | Core Monte Carlo Tree Search logic |
| `3.Model.ipynb` | Neural network architecture (policy + value) |
| `4.AlphaMCTS.ipynb` | AlphaZero-style MCTS integration |
| `5.AlphaSelfPlay.ipynb` | Self-play pipeline |
| `6.AlphaTrain.ipynb` | Neural network training |
| `7.AlphaTweaks.ipynb` | Hyperparameter tuning |
| `8.ConnectFour.ipynb` | Full AlphaZero applied to Connect Four |
| `9.AlphaParallel.ipynb` | Parallel training utilities |
| `10.Eval.ipynb` | Evaluation and benchmarking |

---
## 🧠 Algorithm Summary

AlphaZero works by combining:

✅ Neural Network
- Predicts next move (policy)
- Estimates game outcome (value)

✅ Monte Carlo Tree Search
- Uses neural network predictions to guide exploration
- Balances exploration vs exploitation (PUCT formula)

✅ Self-Play Learning
- Agent plays against itself
- Stores (state, policy, result) samples
- Trains continuously from data

✅ Training Loop
- Self-play games
- Store game history
- Train neural model
- Repeat

