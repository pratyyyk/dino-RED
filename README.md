# dino-RED

A reinforcement learning agent implemented in Python that learns to play the Chrome Dino game using the NEAT (NeuroEvolution of Augmenting Topologies) algorithm.

Overview

This project utilizes a genetic algorithm to train a neural network. The agent operates in real-time, observing the game state and making binary decisions (Jump or Run) to maximize survival time. Through successive generations, the population evolves optimal strategies for obstacle avoidance without pre-programmed rules.

Methodology

The agent is powered by a Feed-Forward Neural Network evolved via NEAT.

Inputs (2):

Dinosaur Y-position (vertical location).

Euclidean distance to the next obstacle.

Outputs (1):

Activation > 0.5 triggers a Jump.

Activation ≤ 0.5 maintains Run state.

Fitness Function: Determined by the distance traveled (score).

Project Structure

.
├── Assets/              # Game sprites (Dino, Cactus, Track)
├── config.txt           # NEAT algorithm parameters
├── main.py              # Entry point and game loop
└── requirements.txt     # Python dependencies


Install dependencies:

pip install -r requirements.txt


Verify Assets:
Ensure the Assets directory contains the required subfolders (Dino, Cactus, Other) and image files.

Usage

Execute the main script to initiate the training simulation:

python main.py


The simulation will launch a window displaying the current generation. The game speed increases automatically as the fitness score rises.

Configuration

The evolutionary parameters are defined in config.txt. Key configurations include:

pop_size: The number of agents per generation (Default: 15).

fitness_threshold: The target score to terminate training.

network parameters: Settings for node mutation, weight initialization, and activation functions.

License

This project is open-source and available under the MIT License.
