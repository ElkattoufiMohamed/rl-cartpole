# Reinforcement Learning: CartPole with Deep Q-Learning

A simple yet powerful implementation of a **Deep Q-Network (DQN)** to solve the classic CartPole-v1 control problem.

The agent learns to balance a pole on a cart through trial and error, maximizing its cumulative reward.

---

## 🚀 Project Overview

- **Goal:** Train an agent to keep the pole balanced as long as possible.
- **Algorithm:** Deep Q-Learning (DQN).
- **Frameworks:** `TensorFlow`, `Gymnasium`, `NumPy`, `Matplotlib`.
- **Key Features:**
    - Epsilon-greedy policy for exploration vs exploitation
    - Replay buffer for stable learning
    - Visualization of training progress
    - Option to render the trained agent

---

## 📂 Project Structure

```
rl-cartpole/
├── notebooks/
│   └── cartpole_dqn.ipynb   # Main Jupyter Notebook
├── .gitignore
└── .venv/                   # Virtual environment (excluded from git)

```

---

## 🛠️ Installation & Setup

1. **Clone the repository:**
    
    ```bash
    git clone https://github.com/ElkattoufiMohamed/rl-cartpole.git
    cd rl-cartpole
    
    ```
    
2. **Create & activate a virtual environment:**
    
    ```bash
    python -m venv .venv
    # macOS/Linux
    source .venv/bin/activate
    # Windows
    .venv\Scripts\activate
    
    ```
    
3. **Install dependencies:**
    
    ```bash
    pip install gymnasium gymnasium[classic_control] tensorflow matplotlib numpy jupyter
    
    ```
    
4. **Launch Jupyter Notebook:**
    
    ```bash
    jupyter notebook
    
    ```
    
    Open `notebooks/rl-cartpole.ipynb` to run the code.
    

---

## 🧠 How It Works

- **State:** `[cart position, cart velocity, pole angle, pole angular velocity]`
- **Actions:** Push cart left (0) or right (1).
- **Reward:** `+1` for every timestep the pole remains upright.
- **Learning:**
    - Predict Q-values with a neural network.
    - Use the Bellman equation to update Q-values.
    - Store experiences in a replay buffer and sample random batches for training.

---

## 📊 Training

- Episodes: `500` (default)
- Batch size: `32`
- Training stops early if the agent averages >450 over the last 100 episodes.

A plot of **Scores vs Episodes** shows the learning curve.

---

## 🎥 Rendering the Agent

After training, you can watch the agent in action:

```python
env = gym.make('CartPole-v1', render_mode='human')
# Use the trained agent to act without exploration

```

---

## 🗺️ Next Steps / Upgrades

- Implement a **Target Network** for stability.
- Try **Double DQN** for better performance.
- Add **Prioritized Experience Replay**.
- Experiment with other environments like `LunarLander-v2` or `Acrobot-v1`.

---

## 📌 Requirements

- Python 3.8+
- `gymnasium`
- `tensorflow`
- `numpy`
- `matplotlib`
- `jupyter`

## 📜 License

This repository contains code for educational/research purposes. Please refer to the licenses of individual models and libraries for their respective terms.

## Contact

If you have any questions or feedback, feel free to reach out:

- GitHub: [ElkattoufiMohamed](https://github.com/ElkattoufiMohamed)
- Email: contact@mohamedelkattoufi.com