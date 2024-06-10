# A3C for Atari Kung Fu Master

This repository implements the Asynchronous Advantage Actor-Critic (A3C) algorithm to train an AI agent to play the Atari game "Kung Fu Master" using PyTorch and Gymnasium.

## Features

- **Custom Neural Network Architecture**: Convolutional layers process game frames, followed by fully connected layers to output action probabilities and state values.
- **Environment Preprocessing**: Efficient frame stacking and resizing for optimal input to the neural network.
- **Asynchronous Training**: Multiple agents are trained in parallel across different environment instances to improve learning efficiency and stability.
- **Hyperparameter Configuration**: Easily adjustable learning rate, discount factor, and number of parallel environments.
- **Evaluation and Visualization**: Tools for evaluating the agent's performance and visualizing gameplay.

## Usage

### Training the Agent

Run the script to start training the A3C agent.

### Evaluating the Agent

Evaluate the performance of the trained agent.

### Visualizing the Results

Visualize the agent's performance by generating a video.

## Code Overview

- **Neural Network Architecture**: Defined in the `Network` class with convolutional and fully connected layers.
- **Environment Preprocessing**: Implemented in the `PreprocessAtari` class to resize and stack frames.
- **A3C Agent**: The `Agent` class handles action selection, network updates, and gradient calculations.
- **Training Script**: Manages asynchronous environment interactions and agent training using the `EnvBatch` class.
- **Evaluation and Visualization**: Includes functions to evaluate agent performance and generate gameplay videos.

## Hyperparameters

- `learning_rate = 1e-4`
- `discount_factor = 0.99`
- `number_environments = 10`

## Examples

An example training session output:

- Observation shape: (4, 42, 42)
- Number actions: 18
- Action names: ['NOOP', 'RIGHT', 'LEFT', 'UP', 'DOWN', 'UPRIGHT', 'UPLEFT', 'DOWNRIGHT', 'DOWNLEFT', 'UPRIGHTFIRE', 'UPLEFTFIRE', 'DOWNRIGHTFIRE', 'DOWNLEFTFIRE', 'RIGHTFIRE', 'LEFTFIRE', 'UPFIRE', 'DOWNFIRE', 'FIRE']
- Average agent reward: 250.0
