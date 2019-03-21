[//]: # (Image References)

[image1]: ./FigurePlot.png "Rewards Plot"

# Project 1: Navigation - Report

### Solution

#### Approach

The first approach was to try a simple DQN learning algorithm described in the class. The code training the agent and network model is in `dqn_agent.py` and `model.py` accordingly.

#### Neural Network Architecture
The network is a 4-layer fully connected neural network with ReLu activation, and with 37 units in the input layer, 64 units in each of the hidden layers and 4 units in the output layer.

#### Hyperparameters
The initial approach used the following hyperparameters:

DQN:
- n_episodes (int): maximum number of training episodes: *2000*
- max_t (int): maximum number of timesteps per episode: *1000*
- eps_start (float): starting value of epsilon, for epsilon-greedy action selection: *1.0*
- eps_end (float): minimum value of epsilon: *0.01*
- eps_decay (float): multiplicative factor (per episode) for decreasing epsilon: *0.995*

Agent:
- BUFFER_SIZE = int(1e5)  
- BATCH_SIZE minibatch size: *64*
- GAMMA: discount factor: *0.99*
- TAU: for soft update of target parameters: *1e-3*
- LR: learning rate: *5e-4*
- UPDATE_EVERY: how often to update the network: *4*

#### Results

The basic DQN with initial hyperparameters performed adequately and trained the agent to solve the environment with average score of 13.07 in 488 episodes.

Rewards Plot:
![Rewards Plot][image1]

### Future work
The simplicy of the environment, even a standard DQN seems to perform adequately. There are some criteria for getting a better agent behaivour additional to experience replay and DDQN like A3C, Distributional DQN among others. If we wanted to experement further, a double DQN, Dueling DQN can be combined in a Rainbow approach.