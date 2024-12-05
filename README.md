# COMPARING RL ALGORITHMS IN PONG GAME

This Repository includes the works done on the Intro to AI course project taught by Dr. Vahid Behzadan.  
Team members: [Amirhossein Karimi](https://www.linkedin.com/in/amirhosseinkarimi24/), [Mary Narouei](https://www.linkedin.com/in/marynarouei/)  

## TABLE OF CONTENTS
- [INTRODUCTION TO PONG GAME](#introduction-to-pong-game)
- [STATEMENT OF PROJECT OBJECTIVES](#statement-of-project-objectives)
- [APPROACH](#approach)
- [DELIVERABELS](#deliverabels)
- [EVALUATION METHODOLOGY](#evaluation-methodology)
- [PREREQUISITES](#prerequisites)
- [INSTALATION](#instalation)
- [USAGE](#usage)
- [CONTRIBUTING](#contributing)


### INTRODUCTION TO PONG GAME

A table tennis–themed twitch arcade sports video game, manufactured by Atari and originally released on 29 November 1972. It is one of the earliest arcade video games.  
Pong is a two-dimensional sports game that simulates table tennis. The player controls an in-game paddle by moving it vertically across the left or right side of the screen. They can compete against another player controlling a second paddle on the opposing side. Players use the paddles to hit a ball back and forth. The goal is for each player to reach eleven points before the opponent; points are earned when one fails to return the ball to the other.

<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/62/Pong_Game_Test2.gif" alt="Pong Game">
</div>
<br>

- **Setup**: The agent controls a paddle, aiming to hit the ball past an AI opponent's paddle.  
- **Rewards**: +1 for scoring.  
- **Observations**: Provides stacked pixel frames as input, often preprocessed.  
- **Actions**: Move up, move down, or stay stationary.  
- **Game End**: The game ends when either the agent or the opponent scores 21 points.  

Pong’s simplicity and challenge in timing and spatial awareness make it ideal for evaluating RL algorithm performance.

### STATEMENT OF PROJECT OBJECTIVES

In the field of deep reinforcement learning, numerous algorithms have been developed, each offering distinct advantages. However, determining the most effective algorithm for specific environments remains a challenge. This project aims to evaluate three widely used algorithms (PPO, DQN, A2C) by testing them in a controlled sample environment (Pong Game). Through a comparative analysis of their performance, we seek to identify and understand the strengths and limitations of each approach.

### APPROACH

The following algorithms have been selected from the available developed methods for this study:

- Proximal Policy Optimization (PPO)
- Deep Q-Network (DQN)
- Advantage Actor-Critic (A2C)<br>

These algorithms will be evaluated in the Pong environment utilizing the rl-baselines3-zoo repository. 
The primary tool used for this project is Jupyter Notebook.
The project code incorporates the following libraries: 
gym, stable-baselines3, box2d-py, pybullet_envs_gymnasium, cloudpickle, plotly, panda-gym, wandb, moviepy, pyvirtualdisplay, pandas, swig, cmake, ffmpeg.

### DELIVERABELS

Step-by-Step implementation instruction for training and evaluating an RL agent in pong environment using our algorithms using rl- baselines3-zoo repository.
- The hyperparameter files of each algorithm
- Final diagrams and comparisons
- A YouTube video with the description of the analysis of the diagrams and the code.

### EVALUATION METHODOLOGY

 After obtaining the results in a CSV file, we will utilize the Matplotlib to visualize the data by plotting reward-steps diagrams for each algorithm under investigation. By comparing these diagrams, we will get the following performance metrics:
- Average Reward
- Stability
- Final Performance
- Sample Efficiency

### PREREQUISITES

- Python (>=3.8)
- You can run this Notebook on Google Colab or your local GPUs. If you are using Google Colab, change the runtime to T4 GPU.

### INSTALATION

To install Project Title, follow these steps:
1. Clone the repository and instal packages:<br>

<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>pip install git+https://github.com/DLR-RM/rl-baselines3-zoo</code></pre>
</div>

2. install aditional packages:<br>


<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>apt-get install swig cmake ffmpeg<br>pip install gymnasium[atari]<br>pip install gymnasium[accept-rom-license]<br>apt install python-opengl<br>apt install ffmpeg<br>apt install xvfb<br>pip3 install pyvirtualdisplay</code></pre>
</div>

### USAGE

We need to have a virtual screen to be able to render the environment: 
<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code># Virtual display
from pyvirtualdisplay import Display
virtual_display = Display(visible=0, size=(1400, 900))
virtual_display.start()</code></pre>
</div>
Before running the training code, you have to create a hyperparameter config file or you can use the default hyperparameters defined by our source.<br>
<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>python -m rl_zoo3.train --algo (Algorithm name)  --env PongNoFrameskip-v4</code></pre>
</div>


and now for evaluating you would have to run the following code:

<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>python -m rl_zoo3.enjoy  --algo (Algorithm name) --env PongNoFrameskip-v4  --no-render  --n-timesteps (number of timesteps) --folder logs/</code></pre>
</div>


### CONTRIBUTING
