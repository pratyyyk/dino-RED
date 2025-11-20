# dino-RED

A Python implementation of the NeuroEvolution of Augmenting Topologies (NEAT) algorithm applied to the classic Chrome Dinosaur endless runner.

## Project Overview
The core of this project is the interaction between the game environment (Pygame) and the evolutionary algorithm (NEAT-Python).

* Evolutionary Strategy: The system begins with a population of random neural networks. Agents that survive longer are assigned higher fitness scores.
* Selection & Mutation: High-performing genomes breed the next generation. The algorithm modifies connection weights and occasionally adds new nodes or connections to the network topology.
* Convergence: Over successive generations, the population converges on an optimal strategy for timing jumps relative to obstacle speed and distance.
