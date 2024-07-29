# Atari_DQN

This project implements Deep Q-Learning (DQN) to train agents to play Atari games. The learning process leverages techniques from DeepMind's research, including replay buffers, frame skipping, and target networks, to handle the complexity of action and state spaces in these games.

## Features

- **Game Playback**: Demonstrates DQN performance on various Atari games.
- **Techniques Used**:
  - **Replay Buffer**: Stores and reuses past experiences to improve learning efficiency.
  - **Frame Skip**: Reduces computational load by skipping frames.
  - **Target Network**: Stabilizes training by using a fixed network for calculating target Q-values.

## Visualization

Explore the results and performance metrics of the DQN model on Atari games [here](https://wandb.ai/senich17/DQN_Atari?nw=nwusersenich17).

## Hyperparameter Tuning

### Learning Rate

- **High Learning Rate**:
  - **Pros**: Faster convergence, which can be beneficial for rapid model development.
  - **Cons**: May lead to instability and fluctuations in the loss function, and can cause the model to skip over optimal solutions.

- **Low Learning Rate**:
  - **Pros**: Provides stable learning with fewer fluctuations.
  - **Cons**: Slower convergence, potentially ineffective in resource-constrained environments, and a higher risk of getting stuck in local minima.

### Buffer Size

- **Small Buffer Size**:
  - **Pros**: Faster learning due to less data processing.
  - **Cons**: Risk of overfitting to frequent examples and potential instability if the buffer does not adequately represent the state space.

- **Large Buffer Size**:
  - **Pros**: More stable learning with a diverse dataset and reduced overfitting risk.
  - **Cons**: Increased training time due to processing more data.

### Additional Resources

For further details and interactive experiments, visit [this Colab notebook](https://colab.research.google.com/drive/14-laEI5JlzRCThZ1U9Y-_uxURCQj3tot?usp=sharing).
