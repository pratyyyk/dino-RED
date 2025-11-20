# 🦕 dino-RUN

The project aims to develop an AI agent capable of playing the Classic Dino endless runner game. This agent learns to play the game from scratch using the NEAT algorithm, goal was to implement a machine learning model that takes environmental inputs and produces an action in real-time.

## 📃 Description 

This is the **Chrome Dino Game** using NEAT and Pygame written in **Python**. 

In this project, NEAT is used to train an AI to play the Chrome Dino Game.This is a simple infinite runner where the player has to jump over cactus and avoid birds. 
The game gets progressively harder as the player's score increases.

## 🧑🏻‍🔧 Technical Architecture

The neural network controlling each dinosaur is a Feed-Forward Network configured as follows:

1. Neural Topology

* Input Layer (2 Nodes):

* Y-Position: The vertical position of the dinosaur (tracking jump height).

* Obstacle Distance: Euclidean distance between the dinosaur and the next incoming obstacle.

* Hidden Layers: Evolved dynamically by the algorithm (starts with 0).

* Output Layer (1 Node):

* Action Trigger: A tanh activation value > 0.5 initiates a JUMP. Otherwise, the agent continues to RUN.

2. Configuration (config.txt)

* Population Size: 15 agents per generation.

* Fitness Function: Maximize distance traveled.

* Activation Function: Hyperbolic Tangent (tanh).

## 🕹️ Controls 

- You don't need to control the dinosaur. The AI will :)

## 📂 Installation

Prerequisites

* Python 3.6+

* pip (Python Package Installer)

# 🍽️ Setup

* Clone the Repository
* install dependencies
* Ensure the Assets/ folder is present in the root directory
* python main.py

## 📚 Libraries 

- pygame: Pygame is a cross-platform set of Python modules designed for writing video games.
- NEAT: NEAT is a method developed by Kenneth O. Stanley for evolving arbitrary neural networks.

## 🪪 Licence

This project is open-source software licensed under the MIT License.




