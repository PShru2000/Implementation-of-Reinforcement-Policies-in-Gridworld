# Evaluating the Effectiveness of Temporal Difference Learning Methods in a Windy Gridworld

## Environment Setup

The Windy Gridworld is a modification of the standard gridworld environment, designed to test reinforcement learning algorithms under conditions of environmental dynamics that affect movement. This particular setup introduces a crosswind that runs upward through the middle of the grid, affecting the agent's trajectory as it moves towards a goal state. The unique challenge in Windy Gridworld lies in the wind's variable strength across different columns of the grid, which shifts the agent's next state upward by a specified number of cells, depending on the column's wind strength.


## Features of the Windy Gridworld:

-**Standard Actions**: The agent has four standard movement options: up, down, right, and left.

-**Wind Effect**: In certain regions of the grid, specifically the middle columns, executing any action results in an additional upward shift, the magnitude of which varies by column and is indicated by the wind strength values below each column.

-**Undiscounted Episodic Task**: The task is episodic with a constant reward of -1 for each action until the goal state is reached, emphasizing the importance of reaching the goal in as few steps as possible.

-**Adaptation Requirement**: Agents must adapt their strategies to account for the wind's influence, making navigation more challenging than in a standard gridworld environment.

![Screenshot](Screenshot%202024-02-03%20121357.png)


## Objectives:

This project aims to explore and evaluate the effectiveness of various Temporal Difference (TD) learning methods within the context of a Windy Gridworld.

**Implementation Objectives:**

- **Windy Gridworld Domain:** Implementing the Windy Gridworld environment, incorporating specific dynamics such as variable wind strength across the grid that influences the agent's movement.

- **TD Learning Methods:** Implementing and integrate a suite of TD learning methods to navigate and solve the Windy Gridworld problem, including:
  
On-policy Monte-Carlo control for ε-soft policies

SARSA (on-policy TD control)

Expected SARSA

n-step SARSA with n set to 4

Q-learning (off-policy TD control)

Optional: Dynamic programming to provide an upper bound on performance
