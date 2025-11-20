#red-Dino

A Python implementation of the NeuroEvolution of Augmenting Topologies (NEAT) algorithm applied to the classic Chrome Dinosaur endless runner.

This project demonstrates an autonomous agent that evolves neural network topologies from scratch to master obstacle avoidance. The agent operates in real-time, learning optimal jump strategies through genetic variation and selection without pre-programmed heuristics.

##Project Overview

The core of this project is the interaction between the game environment (Pygame) and the evolutionary algorithm (NEAT-Python).

Evolutionary Strategy: The system begins with a population of random neural networks. Agents that survive longer are assigned higher fitness scores.

Selection & Mutation: High-performing genomes breed the next generation. The algorithm modifies connection weights and occasionally adds new nodes or connections to the network topology.

Convergence: Over successive generations, the population converges on an optimal strategy for timing jumps relative to obstacle speed and distance.

##Technical Architecture

The neural network controlling each dinosaur is a Feed-Forward Network configured as follows:

1. Neural Topology

Input Layer (2 Nodes):

Y-Position: The vertical position of the dinosaur (tracking jump height).

Obstacle Distance: Euclidean distance between the dinosaur and the next incoming obstacle.

Hidden Layers: Evolved dynamically by the algorithm (starts with 0).

Output Layer (1 Node):

Action Trigger: A tanh activation value > 0.5 initiates a JUMP. Otherwise, the agent continues to RUN.

2. Configuration (config.txt)

Population Size: 15 agents per generation.

Fitness Function: Maximize distance traveled.

Activation Function: Hyperbolic Tangent (tanh).

##Project Structure

The application relies on a strict directory structure for asset loading.

ai-dino-runner/
├── Assets/                  # Required graphic assets
│   ├── Dino/                # DinoRun1.png, DinoRun2.png, DinoJump.png
│   ├── Cactus/              # SmallCactus1-3.png, LargeCactus1-3.png
│   └── Other/               # Track.png
├── config.txt               # NEAT genome configuration
├── main.py                  # Application entry point
├── requirements.txt         # Dependency manifest
└── README.md                # Documentation


##Install dependencies:

pip install -r requirements.txt


##Asset Verification:
Ensure the Assets/ folder is present in the root directory. The simulation will fail to initialize if sprites are missing.

##Usage

To start the training simulation:

python main.py


Runtime Controls

The simulation runs automatically. The HUD displays:

Points: Current score (distance traveled).

Dinosaurs Alive: Count of active agents in the current generation.

Generation: Current evolutionary iteration.

Game Speed: dynamic velocity multiplier.

##License

This project is open-source software licensed under the MIT License.
