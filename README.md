[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Navigation

### Project Details

The goal of the project is to train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.


### Getting Started
 
The environment requires the following libraries:

```
unityagents
gym
torch
numpy
matplotlib
```

The required libraries can be installed with:

```bash
pip install unityagents gym torch numpy matplotlib
```

and the environment can be downloaded from the instructions in the following location:
https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation


### Instructions

Follow the instructions in `Navigation.ipynb` to get started with training your own agent! 

After trainig the model, parameters will be dumpt to `checkpoint.pth` and will be used by the trained agent.
