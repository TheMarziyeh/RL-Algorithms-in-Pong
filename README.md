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
- [CONTACT US](#contact-us)

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

- Proximal Policy Optimization (PPO-Clip)
- Deep Q-Network (Vanilla-DQN)
- Advantage Actor-Critic (A2C)<br>

These algorithms will be evaluated in the Pong environment utilizing the rl-baselines3-zoo repository. 
The primary tool used for this project is Jupyter Notebook.

### DELIVERABELS

Step-by-Step implementation instruction for training and evaluating an RL agent in pong environment using our algorithms using rl-baselines3-zoo repository.
- The hyperparameter files of each algorithm
- Final diagrams and comparisons
- A YouTube video with the description of the analysis of the diagrams and the code.

### EVALUATION METHODOLOGY

 After obtaining the results in a CSV file, we will utilize the `Matplotlib` to visualize the data by plotting reward-steps diagrams for each algorithm under investigation. By comparing these diagrams, we will get the following performance metrics:
- Average Reward
- Stability
- Final Performance
- Episode Length

### PREREQUISITES

- `Python (>=3.8)`
- You can run this Notebook on Google Colab or your local GPUs. If you are using Google Colab, change the runtime to T4 GPU.

### INSTALATION

In this project, we are using "rl-baselines3-zoo". You can use the [GitHub repository](https://github.com/DLR-RM/rl-baselines3-zoo) and [Documentation](https://rl-baselines3-zoo.readthedocs.io/en/master/guide/quickstart.html), or you can follow these steps:
1. Clone the repository and instal packages:<br>

<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>git clone https://github.com/DLR-RM/rl-baselines3-zoo<br>
cd rl-baselines3-zoo/<br>
pip install -e .</code></pre>
</div>

2. Install the additional packages for full installation:<br>

<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>apt-get install swig cmake ffmpeg<br>
pip install -r requirements.txt<br>
pip install -e .[plots,tests]<br></code></pre>
</div>

### USAGE

Before running the training code, you have to create a hyperparameter config file(yml file) or you can use the default hyperparameters defined by the source.<br> You can train your agent using the following code:
<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>python -m rl_zoo3.train --algo (Algorithm name)  --env PongNoFrameskip-v4 --conf-file (Location of config file)</code></pre>
</div>
If you want to use the default hyperparameters, remove "--conf-file (Location of config file)".

For evaluating your trained agent, you would have to run the following code:
<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>python -m rl_zoo3.enjoy  --algo (Algorithm name) --env PongNoFrameskip-v4  --no-render  --n-timesteps (number of timesteps) --folder logs/</code></pre>
</div>

To record a video of your best saved model's performance, you can use this code:
<div><button onclick="copyToClipboard('codeBlock1')"></button><pre id="codeBlock1"><code>python -m rl_zoo3.record_video  --algo (Algorithm name) --env PongNoFrameskip-v4  --load-best  --n-timesteps (number of timesteps)  --folder logs/</code></pre>
</div>


### CONTRIBUTING

As mentioned before this is a final project for Introduction to Artificial intelligence course done in University of New Haven, **Fall 2024**. So any updates, enhancement or contribution is greatly appriciated! If you'd like to contribute to our project, here are some guidelines:

1. Fork the repository.
2. Create a new branch for your changes.
3. Write tests to cover your changes.
4. Run the tests to ensure they pass.
5. Commit your changes.
6. Push your changes to your forked repository.
7. Submit a pull request.

### CONTACT US

If you have any questions regarding this project please feel free to contact us through email or Linkedin! We will be happy to help :) <br>
*[Amirhossein](https://www.linkedin.com/in/amirhosseinkarimi24/): akari9@unh.newhaven.edu<br>*
*[Mary](https://www.linkedin.com/in/marynarouei/): mnaro4@unh.newhaven.edu*

