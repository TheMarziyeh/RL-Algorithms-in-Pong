# COMPARING RL ALGORITHMS IN PONG GAME

This Repository includes the works done on the Intro to AI course project taught by Dr. Vahid Behzadan.  
Team members: [Amirhossein Karimi](https://www.linkedin.com/in/amirhosseinkarimi24/), [Mary Narouei](https://www.linkedin.com/in/marynarouei/)  
University Of New Haven  
Fall 2024  

## INTRODUCTION TO PONG GAME

A table tennis–themed twitch arcade sports video game, manufactured by Atari and originally released on 29 November 1972. It is one of the earliest arcade video games.  
Pong is a two-dimensional sports game that simulates table tennis. The player controls an in-game paddle by moving it vertically across the left or right side of the screen. They can compete against another player controlling a second paddle on the opposing side. Players use the paddles to hit a ball back and forth. The goal is for each player to reach eleven points before the opponent; points are earned when one fails to return the ball to the other.

<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/62/Pong_Game_Test2.gif" alt="Pong Game">
</div>

- **Setup**: The agent controls a paddle, aiming to hit the ball past an AI opponent's paddle.  
- **Rewards**: +1 for scoring.  
- **Observations**: Provides stacked pixel frames as input, often preprocessed.  
- **Actions**: Move up, move down, or stay stationary.  
- **Game End**: The game ends when either the agent or the opponent scores 21 points.  

Pong’s simplicity and challenge in timing and spatial awareness make it ideal for evaluating RL algorithm performance.

## STATEMENT OF PROJECT OBJECTIVES

In the field of deep reinforcement learning, numerous algorithms have been developed, each offering distinct advantages. However, determining the most effective algorithm for specific environments remains a challenge. This project aims to evaluate three widely used algorithms (PPO, DQN, A2C) by testing them in a controlled sample environment (Pong Game). Through a comparative analysis of their performance, we seek to identify and understand the strengths and limitations of each approach.

## APPROACH

The following algorithms have been selected from the available developed methods for this study:
