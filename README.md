# Atari_DQN
Learning based on the deep Q-network

## Playback of DQN results on Atari games.

* Some games may require specific methods (for example, Montezuma's Revenge, etc.)
* Techniques from the DeepMind article are used: replay buffer, frame skip, target network.
* In many cases, tabular reinforcement learning methods do not cope with the space of actions and states.
* To generalize the values of the utility function to unobservable states, an approximation is used
* The idea is to use the use case memory (replay buffer).
 
## Visualization

[https://wandb.ai/senich17/DQN_Atari?nw=nwusersenich17]

## Conclusions on hyperparameters

### Learning rate

* High value:
Fast convergence: The model can converge quickly at the beginning of training, which is useful when you need to quickly get a working model.
Instability: Instability may occur in the learning process, manifested as fluctuations or even a decrease in the loss function.
Skipping optimal solutions: Too large steps can cause the model to "jump" over optimal points.

* Low learning_rate:
Stability: Provides more stable learning, with less fluctuations in the process.
Slow convergence: Can significantly slow down the learning process, which is ineffective in resource-limited settings.
Risk of getting stuck in local minima: With a very low learning_rate, there is a risk that the model will get stuck in the local minimum and will not reach the best solution.

### Buffer size

* Small buffer_size:
Fast learning: The agent learns faster because training takes place on less data, which requires less processing time.
Over-training risk: An agent may begin to retrain on frequently occurring examples in the buffer, which will impair its ability to generalize behavior in new or rarely encountered situations.
Learning instability: Learning can become more unstable if the experience in the buffer is not representative enough for the entire state space.

* Large buffer_size:
Learning Stability: Learning becomes more stable by using a more diverse and representative dataset.
Reduction of over-training: A larger buffer reduces the likelihood of over-training, as the agent uses a wider and more diverse set of experiences for training.
Increased training time: Processing more data can increase the time required for training, as each data packet requires more processing time.

### Additional

[https://colab.research.google.com/drive/14-laEI5JlzRCThZ1U9Y-_uxURCQj3tot?usp=sharing]
