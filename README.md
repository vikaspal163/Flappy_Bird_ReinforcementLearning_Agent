# 🐦 Flappy Bird Reinforcement Learning Agent

A **Deep Q-Network (DQN)** based Reinforcement Learning agent that learns to play Flappy Bird using Python and PyTorch.

---

## 🚀 Project Overview

This project implements a Reinforcement Learning (RL) agent that interacts with a Flappy Bird environment and learns to maximize its score through trial and error.

The agent is trained using **Deep Q-Learning**, a popular RL algorithm where a neural network approximates the optimal action-value function. ([GitHub][1])

---

## 🧠 Key Features

* Deep Q-Network (DQN) implementation
* Experience Replay for stable learning
* Target Network synchronization
* Epsilon-greedy exploration strategy
* Configurable hyperparameters using YAML
* Automatic device selection (CPU / CUDA / MPS)
* Training + Inference modes

---

## 🛠️ Tech Stack

* Python
* PyTorch
* Gymnasium
* flappy-bird-gymnasium

---

## 📂 Project Structure

```bash
.
├── agent.py               # Main training and testing logic
├── dqn.py                 # Neural network (Q-network)
├── experience_replay.py   # Replay memory buffer
├── parameters.yaml        # Hyperparameters
├── runs/                  # Logs & trained models
```

---

## ⚙️ Installation

```bash
git clone https://github.com/vikaspal163/Flappy_Bird_ReinforcementLearning_Agent.git
cd Flappy_Bird_ReinforcementLearning_Agent
pip install -r requirements.txt
```

---

## ▶️ Usage

### 🔹 Train the Agent

```bash
python agent.py <param_set> --train
```

Example:

```bash
python agent.py default --train
```

---

### 🔹 Run Trained Agent

```bash
python agent.py <param_set>
```

This will load the trained model and render gameplay.

---

## 🧪 How It Works

### 1. Reinforcement Learning Loop

The agent follows a standard RL cycle:

* Observe state
* Take action
* Receive reward
* Update policy

This interaction helps the agent learn optimal behavior over time. ([LiquidSLR][2])

---

### 2. Deep Q-Learning

The agent learns a Q-function:

```
Q(s, a) → expected future reward
```

* Uses neural network approximation
* Optimized using Mean Squared Error loss

---

### 3. Experience Replay

Transitions are stored as:

```
(state, action, reward, next_state, done)
```

* Random sampling improves stability
* Breaks correlation between consecutive states

---

### 4. Target Network

A separate network is used to:

* Stabilize training
* Reduce oscillations

---

### 5. Exploration Strategy

Uses **epsilon-greedy policy**:

* High randomness initially
* Gradually shifts to exploitation

---

## 📊 Hyperparameters

Defined in `parameters.yaml`:

* Learning rate (`alpha`)
* Discount factor (`gamma`)
* Epsilon decay
* Replay memory size
* Batch size
* Target network update frequency

---

## 💾 Outputs

* 📄 Logs → `runs/<param_set>.log`
* 🧠 Model → `runs/<param_set>.pt`

---

## 📈 Sample Output

```
Episode 1 | Reward = 5 | Epsilon = 1.0
Episode 100 | Reward = 50 | Epsilon = 0.2
Episode 300 | Reward = 120 | Epsilon = 0.05
```

---

## 🔮 Future Improvements

* Double DQN
* Dueling DQN
* Prioritized Experience Replay
* PPO / Actor-Critic methods
* Training visualization (graphs)

---

## 🤝 Contributing

Contributions are welcome!
Feel free to open issues or submit pull requests.

---

## 📜 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

**Vikas Pal**
GitHub: https://github.com/vikaspal163

---

## ⭐ If you like this project

Give it a ⭐ on GitHub!

---

[1]: https://github.com/yenchenlin/DeepLearningFlappyBird?utm_source=chatgpt.com "GitHub - yenchenlin/DeepLearningFlappyBird: Flappy Bird hack using Deep Reinforcement Learning (Deep Q-learning)."
[2]: https://liquidslr.github.io/blog/reinforcement-learning/?utm_source=chatgpt.com "Flappy Bird Game Using Reinforcement Learning | Personal Blog"
