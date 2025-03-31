# Traveling Salesman Problem (TSP) Solver with Genetic Algorithm

![TSP Genetic Algorithm Evolution](example_evolution.gif)

## Overview
This notebook was created as an university assignment, and expanded on a little bit, because I was curious :)
The solution uses a Genetic Algorithm to solve TSP, finding an optimal route that visits all cities once and returns to the origin with minimal distance.

## Features
- Multiple strategies for selection, crossover, mutation, and inheritance
- Adjustable population parameters and evolution settings
- Generation progress visualization
- GIF creation capability
- Convergence detection

## Installation
```bash
pip install numpy matplotlib pillow2
```
```python
# Problem Setup
CITY_COUNT = 50          # Number of cities
LIMIT_X = 300            # Max X coordinate
LIMIT_Y = 300            # Max Y coordinate

# Algorithm Parameters
SPECIMEN_COUNT = 300     # Population size
MAX_GENERATIONS = 200    # Max iterations
TOURNAMENT_SIZE = 3      # Selection pressure
CROSSOVER_RATE = 0.98    # Crossover probability
MUTATION_START_RATE = 0.1
MUTATION_END_RATE = 0.7
```
# **Configuration Options**

## **Selection Methods**  
**Available:** `'tournament'` (default), `'roulette'`, `'random'`  
```python
parents = select_specimens(
    generation,
    selection_type='tournament',
    tournament_size=3
)
```
## **Crossover Methods**  
**Available:** `'order'` (default), `'heuristic_order'`, `'hybrid_order'`
```python
child = crossover_parents(
    parent1,
    parent2,
    crossover_type='heuristic_order',
    max_perm=5
)
```
## **Mutation Methods**  
**Available:** `'swap'` (default), `'shuffle'`, `'heuristic'`

```python
mutated = mutate_spec(
    specimen,
    mutation_type='heuristic',
    max_perms=4
)
```

