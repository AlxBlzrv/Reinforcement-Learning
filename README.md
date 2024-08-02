# Reinforcement Learning with Q-Learning on the Taxi-v3 Environment

## Introduction

### Reinforcement Learning (RL)

Reinforcement Learning (RL) is a branch of machine learning where an agent learns to make decisions by interacting with an environment. Unlike supervised learning, where the model is trained on a dataset with known outputs, RL involves learning through trial and error. The agent takes actions in an environment, receives rewards or penalties, and adjusts its strategy to maximize cumulative rewards over time.

### Q-Learning

Q-Learning is a popular model-free reinforcement learning algorithm used to find the optimal action-selection policy for a given finite Markov decision process (MDP). It operates by learning the value of state-action pairs, which is denoted as Q-values. The goal of Q-Learning is to iteratively update these Q-values based on the agent's experiences to converge to the optimal policy.

The Q-Learning algorithm follows these key steps:
1. Initialize the Q-table with zeros.
2. For each episode, select actions based on an exploration-exploitation strategy (ε-greedy).
3. Update the Q-values using the Bellman equation.
4. Repeat until the policy converges or a predefined number of episodes is reached.

## Taxi-v3 Environment

The Taxi-v3 environment is a classic problem used in Reinforcement Learning to test and demonstrate various algorithms. In this environment, the agent must navigate a grid world to pick up and drop off passengers at designated locations. The state space consists of the location of the taxi, the passenger's location, and the destination. The agent has a set of actions it can perform, including moving in different directions and picking up or dropping off the passenger.

The objective is to learn a policy that maximizes the total reward over time by efficiently navigating the grid and performing the required tasks.

## Project Overview

This project involves applying the Q-Learning algorithm to the Taxi-v3 environment to develop an optimal policy for the agent. The key components of this project are as follows:

1. **Environment Setup**: Using the `gym` library to create the Taxi-v3 environment.
2. **Q-Learning Implementation**: Training the agent using Q-Learning with parameters such as learning rate (α), discount factor (γ), exploration rate (ε), and their decays.
3. **Training the Agent**: Running multiple episodes to update the Q-table and improve the agent's policy.
4. **Evaluation**: Testing the trained agent's performance and calculating average rewards over test episodes.
5. **Visualization**: Creating a GIF animation to visualize the agent's performance and its interactions with the environment.

## How to Run

1. **Install Dependencies**: Ensure you have the required libraries installed. You can install them using pip:
    ```bash
    pip install numpy gym matplotlib pillow
    ```

2. **Run the Code**: Execute the provided Python script to train the agent, evaluate its performance, and generate the GIF animation of the agent navigating the Taxi-v3 environment.

3. **View the Results**: After training, the script will display a GIF animation showing the agent's performance in the environment.

## Code Explanation

- **Environment Creation**: Initializes the Taxi-v3 environment.
- **Q-Learning Parameters**: Configures learning parameters such as α, γ, ε, ε_decay, and min_epsilon.
- **Training Loop**: Runs episodes to update the Q-table based on the agent's interactions with the environment.
- **Evaluation**: Measures the average reward over multiple test episodes to assess the agent's performance.
- **Animation Creation**: Generates a GIF animation to visualize the agent's behavior in the environment.

## Files Included

- `taxi_q_learning.py`: The main script implementing the Q-Learning algorithm, training the agent, and generating the GIF animation.
- `taxi_animation.gif`: A GIF animation visualizing the agent's performance in the Taxi-v3 environment.
- `README.md`: This README file providing an overview of the project, instructions, and details.
- `LICENSE`: The license file for the project.
- **Q-Value Update Formula**: The formula to update the Q-values in Q-Learning.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
