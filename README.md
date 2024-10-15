# maze-problem-using-genetic-algorithm-optimization

### Overview
This project demonstrates the use of genetic algorithms to solve maze problems by evolving potential solutions over multiple generations. The algorithm uses a fitness-based selection mechanism to guide the population toward optimal paths.

# Genetic Algorithm for Maze Solving

This project implements a genetic algorithm (GA) to solve a maze using a 7x20 grid. The aim is to navigate from a start point to the goal, avoiding obstacles and minimizing infeasible steps. The algorithm works by generating a population of potential solutions, evolving through crossover and mutation, and selecting the best solution based on fitness criteria.

## Prerequisites

Install the required Python package `pyamaze`:

```
pip install pyamaze 
```

## Project Structure
**Maze Size**: The maze is a 7x20 grid with a start point at (1, 1) and a goal at (7, 19).
**Algorithm Parameters**:
  Population Size: 2000
  Max Generations: 5000
  Mutation Probability: 0.06
  Crossover Rate: 0.7
  Mutation Length: 15

## Functionality
### Maze Loading
The maze structure is loaded from a CSV file `myMaze.csv`, where each cell in the maze has walls (East, West, North, South) defined for its possible movements.

### Genetic Algorithm Components
1. **Genome**: Each genome represents a path through the maze, encoded as a list of integers.
2. **Population**: The algorithm maintains a population of genomes that evolve over generations to find the best solution.
3. **Fitness Function**: Measures the quality of a solution based on path length, infeasible steps, and distance to the goal.
4. **Crossover**: The `mod7_crossover` function creates new genomes by combining two parent genomes with a mod7 operation.
5. **Mutation**: The `segmented_mutation` function randomly alters a segment of the genome with a specified probability.

### Evolution Loop
The genetic algorithm evolves the population through multiple generations. Each generation undergoes fitness evaluation, selection of the best solutions, crossover, and mutation.

### Solution
If a solution is found within the specified number of generations, the path is traced and visualized using the pyamaze library.

## How It Works
1. Load Maze: The maze is loaded from the CSV file into the program.
2. Generate Initial Population: A population of random genomes is generated.
3. Evaluate Fitness: Each genome is evaluated for fitness based on path feasibility and distance to the goal.
4. Evolve Population: Through crossover and mutation, the population evolves over generations.
5. Solution: The best genome is traced and visualized as the solution path.

### Example Usage
```
main()
```
