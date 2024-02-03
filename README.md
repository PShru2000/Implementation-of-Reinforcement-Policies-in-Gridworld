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

- **Windy Gridworld Domain:** Implementing the Windy Gridworld environment, incorporating specific dynamics such as variable wind strength across the grid that influences the agent's movement.

- **TD Learning Methods:** Implementing and tesing the effectiveness of TD learning methods to navigate and solve the Windy Gridworld problem, including:
  
  - On-policy Monte-Carlo control for ε-soft policies

  - SARSA (on-policy TD control)
    
  - Expected SARSA
    
  - n-step SARSA with n set to 4
  
  - Q-learning (off-policy TD control)
    
  - Optional: Dynamic programming to provide an upper bound on performance
 

#### Enhanced Action Space
- **Objective:** Implement and assess the impact of King's Moves (eight directions plus an optional no-movement action) on navigation efficiency in the Windy Gridworld. Determine the effectiveness of expanded action choices in improving path optimization and strategy under windy conditions.

#### Stochastic Wind Effects
- **Objective:** Introduce stochastic wind effects to the Windy Gridworld, creating variability in wind influence on movement.Evaluate how TD learning methods adapt to and perform under the unpredictability of wind effects, enhancing understanding of algorithm robustness.

## Output Analysis:

Please refer to the **[outputs]([URL](https://github.com/PShru2000/Implementation-of-Reinforcement-Policies-in-Gridworld/tree/main/outputs%20-RL))** folder for results

The provided plots represent the performance of different Temporal Difference (TD) learning methods applied to the Windy Gridworld environment, the Windy Gridworld with King's moves (allowing eight possible actions), and the stochastic Windy Gridworld with King's moves

### Windy Gridworld Environment 
- **SARSA, Q-learning, Expected SARSA, n-step SARSA,** and **ε-soft Monte Carlo** methods all show improvement over time, as indicated by the increasing number of episodes completed within a given number of timesteps. This suggests that all methods are learning effective policies for navigating the gridworld.
- The confidence bands indicate that while there is variability in performance across trials, the general trend for all methods is positive.
- There's a noticeable convergence of methods as the number of timesteps increases, which may imply that all methods are approaching an optimal policy.

### Windy Gridworld with King's Moves
- The introduction of diagonal moves (King's moves) appears to allow for faster completion of episodes across all methods. This is evident from the steeper slopes in the early timesteps compared to the standard environment.
- The methods still show a converging trend, but with a tighter confidence band, suggesting that the additional actions help stabilize the learning process across trials.

### Stochastic Windy Gridworld with King's Moves
- The introduction of stochastic wind adds complexity, which seems to slow down the learning process for all methods, as indicated by fewer episodes completed in the initial timesteps compared to deterministic environments.
- Over time, however, the methods adapt to the stochasticity, and a gradual improvement is observed.
- The confidence bands are much wider in the stochastic environment, highlighting increased variability in performance likely due to the random nature of the wind.

### Overall Analysis
- All TD learning methods are capable of adapting to the complexities of the Windy Gridworld and its variants, with noticeable learning and improvement over time.
- The addition of King's moves enhances performance, suggesting that a richer action space can significantly benefit policy learning in such environments.
- Stochasticity increases initial variability and learning complexity but does not prevent the methods from eventually learning effective policies.
- Among the methods, **Q-learning** often shows a superior performance, especially in the presence of stochasticity, which aligns with its off-policy nature and general robustness.

 

