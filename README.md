## Multi Agent Reinforcement Learning - Training using Deep Deterministic Policy Gradient (DDPG)

### Background

Train multiple agents using Deep Deterministic Policy Gradient Reinforcement Learning to train a double jointed arm to move to target locations.  

![Double Jointed Arm Movement](https://video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif)

There is a reward of +0.1 for each step that the agent's hand is in the goal location. So the goal of the agent is to maintain its position at the target location for as many timesteps as possible.

 This Reacher environment has been kindly provided by Unity is provided by [Unity Machine Learning agents]([https://github.com/Unity-Technologies/ml-agents](https://github.com/Unity-Technologies/ml-agents)). 

#### State Space

The observation space has 33 variables corresponding to position, rotation, velocity and angular velocities of the arm. 
#### Action Space

Each action is a vector with four numbers corresponding to the torque applicable to the two joints. 

Every entry in the action vector should be a number between -1 and 1.

#### When Solved

In order to solve this environment the agent must get an average of +30 over 100 consecutive episode

### Distributed Training

We were provided with two separate version of the Unity environment, a single agent and another version which had 20 identical agents each with its own copy of the environment. The distributed version is useful for algorithms like DDPG where we can use multiple (non-interacting and parallel) copies of the same agent to distribute the task of gathering experience.

### Getting Started


#### Install Dependencies and needed files

The project was finally completed using the Udacity's workspace environment enabled with GPU support. The workspace environment uses the Unity ML-Agent v0.4 interface. 

We would strongly recommend using the ML-Agent v0.4 interface as attempts to download the provided environment , grpcio, Pytorch modules with the latest version of Python installed, were not successful.
##### Dependencies
- Python 3
- Pytorch
- Unity ML-Agents v0.4
- Jupyter 

### Instructions

#### Files
- `Continuous_Control.ipynb` : The main Jupyter notebook to execute the training.
- `ddpg_agent.py`: The multi-agent implementation of the Actor Critic Reinforcement Learning as as outlined in the paper [Continuous Control with Deep Reinforcement Learning](https://arxiv.org/pdf/1509.02971)
- `model.py` : The neural networks for the Actor and Critic 
- `Actor_Model_Checkpoint.pth`:  The trained checkpoints for the Actor model. Load the checkpoints to avoid training the model from scratch. 
- `Critic_Model_Checkpoint.pth`: The trained checkpoints for the Critic model. Load the checkpoints to avoid training the model from scratch.

#### Training the Agent

Follow the exercises in `Continuous_Control.ipynb` to train your agent using multi-agent DDPG
