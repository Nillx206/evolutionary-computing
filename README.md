# Evolutionary Robotics: Evolving Robot Bodies and Brains

Group projects for the **Evolutionary Computing** course (MSc AI, Vrije Universiteit Amsterdam, 2026).
Built on [ARIEL](https://github.com/ci-group/ariel), the evolutionary robotics framework of the VU Computational Intelligence Group, with MuJoCo physics simulation.

## Projects

### 1. Evolving robot morphologies (`assignment1/`)
An evolutionary algorithm that evolves tree-encoded modular robot bodies toward five target morphologies.
- **Fitness:** mean + standard deviation of the tree edit distance to the target bodies (lower is better)
- **Experiment:** two EA variants with different mutation rates, 5 independent seeds each

### 2. Neuroevolution for targeted locomotion (`assignment2/`)
An EA that evolves the weights of a neural-network controller (one hidden layer, tanh) steering a simulated robot toward a target.
- **Fitness:** final distance to target (lower is better)
- **Research question:** how does tournament selection pressure (k = 2 vs. k = 6) affect performance?
- **Baselines:** equal-budget random search and a non-evolved controller, with significance tests across seeds

## My contributions
- **Assignment 1:** parent selection and crossover operators (`parent_selection.py`, `crossover.py`)
- **Assignment 2:** simulation environment and fitness function (`simulation.py`)

## Team
Nikoleta Raychinova, Ada Bilici, Feyza Kurt, Elif Sena Shen

## Running
Requires Python ≥ 3.12 and [uv](https://docs.astral.sh/uv/).
    uv sync
    uv run python assignment1/main.py
    uv run python assignment2/code/experiments.py

The `src/` folder contains the ARIEL framework (GPL-3.0), provided by the course.
