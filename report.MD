# Report: Deep Reinforcement Learning Nanodegree Project 3 Collaboration and Competition
### DDPG

In the implementation, the DDPG is utilized.
- DDPG is a model-free off-policy algorithm for learning continuous actions. It contains an **actor network** and a **critic network**. The DDPG is capable of dealing with continuous action domain. The algorithm is listed below:
![deep_q_algorithm](DDPG.png)
- DDPG is closely related to Q-learning: if you know the optimal action-value function **Q<sup>\*</sup> (s,a)**, then in any given state, the optimal action a<sup>\*</sup> (s) can be found by **a<sup>\*</sup> (s)=argmax Q<sup>\*</sup> (s,a)**.

The facts about DDPG are listed below:
- DDPG is an off-policy algorithm
- DDPG can only be used for environments with continuous action space.
- DDPG can be though of as being deep Q-learning for continuous action spaces.

### Network Architectures
The **actor network** includes input layer(24), 2 hidden layer(400,300) and the output layer(2).
The **critic network** include input layer(24), 2 hidden layer(400,300) and the output layer(1). 
DDPG require a target and local network for both **actor network** and **critic network**. Target and local network have same structures. 

### Hyperparameters
In this deep network, the hyperparameters are listed as follows:
- Learning rate for actor= 1e-3
- Learning rate for critic 1e-3
- discount factor = 0.99
- buffer size = 1e6
- batch size = 128
- soft update parameter TAU = 1e-3

### Plots of Rewards
![Plots of Rewards](score.png)
### Idea for future work
To further improve the performance of the agent, we have a few options:
- GAE
- A3C
- PPO