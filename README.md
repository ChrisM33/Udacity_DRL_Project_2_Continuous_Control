
<hr>

<center><font size="6">
<a href="https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893/">Udacity Deep Reinforcement Learning Nanodegree Program</a></font></center>
<br>
<p></p>
<center><font size="6">Project: Continuous Control</font></center>
<p></p>
<br>
<center><font size="3">
<a href="https://gh.linkedin.com/in/christian-motschenbacher-7a660b123/">Christian Motschenbacher</a></font></center>
<br>

<div class="alert alert-block alert-info" style="margin-top: 20px">
<a href="https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893"><img src = "media/UdacityDRL01.png" width = 950, align = "center"></a>
</div>

<hr>

# Table of Contents

<div class="alert alert-block alert-info" style="margin-top: 20px">
<li><a href="#ref1">Author, Project and Environment description </a></li>
<li><a href="#ref2">Getting Started and Dependencies </a></li>
<li><a href="#ref3">Instructions how to run the code </a></li>
<li><a href="#ref4">Resources and References </a></li>
</div>

<hr>

# Author, Project and Environment description
## Author  
  
**Name: [Christian Motschenbacher](https://gh.linkedin.com/in/christian-motschenbacher-7a660b123)**  
  
**Date: 02/2019**  
  
**Project: Udacity Deep Reinforcement Learning Nanodegree Program: Project 2: Continuous Control**  
**This file contains the training and testing code for this project.**


## Project and Environment description

<div style="text-align: justify">  
The task of this project was to train 20 agents, who moves a double-jointed arm to target location and keeps the agent's hand in the goal location. The following video is showing how a trained agent is performing this task well.
</div>

![](./media/UdacityDRL02.gif)
<br>
<div style="text-align: justify">  
A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.
</div>
<br>
<div style="text-align: justify">  
The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.
</div>
<br>
<div style="text-align: justify">  
The task is episodic and in order to solve the environment, the agent must achieve an average score of +30 over 100 consecutive episodes.
</div>
<br>
<div style="text-align: justify">  
For the soution of this task it has been used the Unity ML-Agents Reacher Environment from Unity-Technologies, the Python programming language as well the libraries NumPy, PyTorch and others.</p>
</div>

<hr>

# Getting Started and Dependencies
<br>
<div style="text-align: justify">  
This DRL project use three main software components.
Those components are Python, Udacity DRL course dependencies and as well the Unity-Technologies/ml-agents dependencies. The installations of those elements are described in the following subsections.
</div>

## Python  
  
In order to set up the python environment run the following code and follow the instructions below.

<div style="text-align: justify">  
<br>    
<b>Create (and activate) a new environment with Python 3.6 including the anaconda packages.</b><br>
The following code state how to install python on Linux, Mac or Windows.
In order to install python on your target system you must write or copy paste the following command into the command line of your system.
</div>

The three code commands in the following code sections do the following.
1. Install python and the anaconda packages into the new environment with the name drlnd.
2. Activate the new created environment
3. Deactivate the environment

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6 anaconda  
	source activate drlnd  
    conda deactivate  
	```
	- __Windows__:   
	```bash
	conda create --name drlnd python=3.6 anaconda  
	activate drlnd  
    deactivate  
	```

<div style="text-align: justify">  
<b>Note: Activation and deactivation of the environment.</b><br>
Command (... activate drlnd): This command needs to be executed before any additional python library will be installed into this environment.  
Command (... deactivate): This command needs to be executed before the user will work with another environment.
</div>
<br>
<div style="text-align: justify">  
For the setup of this project once the first command has been executed the environment can be activated and be activated until all dependencies have been installed. 
</div>
<br>
<div style="text-align: justify">  
<b>Download this repository</b><br>
Before you continue with the next dependencies download this repository onto your local computer, in order to continue with the following sections.
</div>

## Udacity DRL course    
<br>
<div style="text-align: justify">  
For easier setup of this project the Udacity DRL course dependencies has been extracted from the repository <a target="_blank" href="https://github.com/udacity/deep-reinforcement-learning">deep-reinforcement-learning</a> and copied into this repository. Therefore, the user can navigate into the folder <b>"./Installation/DRL_Environment/python"</b> of this downloaded repository and perform the command <b>"pip install . "</b> in the command line on the local PC to install the dependencies. More information about the installation if needed can be found at the above linked Udacity repository.
</div>

## Unity-Technologies/ml-agents
<br>
<div style="text-align: justify">  
For easier setup of this project the Unity-Technologies/ml-agents dependencies has been extracted from the repository <a target="_blank" href="https://github.com/Unity-Technologies/ml-agents">Unity-Technologies/ml-agents</a> and copied into this repository. Therefore, the user can navigate into the folder <b>"./Installation/Unity_Technologies_ml_agents/ml-agents/"</b> of this downloaded repository and perform the command <b>"pip install -e . "</b> in the command line on the local PC to install the dependencies. More information about the installation if needed can be found at the above linked Unity-Technologies/ml-agents repository.
</div>

## Unity-Technologies Environment
<br>
<div style="text-align: justify">  
For this project, you will <b>not</b> need to install Unity - this is because the environments for the different operating systems have already been build for you and you can download it from the links below. You need only select the environment that matches your operating system:
</div>

<ul>
<li>Linux: <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip">click here</a></li>
<li>Mac OSX: <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip">click here</a></li>
<li>Windows (32-bit): <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip">click here</a></li>
<li>Windows (64-bit): <a target="_blank" href="https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip">click here</a></li>
</ul>

<div style="text-align: justify">  
Then, place the file in the <b>"./env/"</b> folder of this downloaded GitHub repository and unzip (or decompress) the file.
</div>

<div style="text-align: justify">  
<p>(<b>For Windows users</b>) Check out <a target="_blank" href="https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64">this link</a> if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.</p>
</div>

## Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
Run the following code in your command line of your computer to create an **IPython kernel** for your notebook.
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

## Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu.  
<img src = "media/UdacityDRL03.png" width = 550, align = "center">



<hr>

# Instructions how to run the code
Once you have installed the previous dependencies you can continue with the following instruction on how to run the code.

## Run the code in training and test mode

### Notebook with training and testing code
<br>
<div style="text-align: justify">  
The notebook <b>Continous_Control_solution_training_testing.ipynb</b>, which is in the <b>root folder of this repository</b>, contains the testing and training code of the agent in the environment. The fist part explains and shows the performance (testing) of an untrained agent, the middle part of this file explains how to train the agent and the bottom part of this file explains and shows the performance (testing) of an trained agent. It is not required to run the whole notebook from the beginning in order to run the testing section, because the training weights file of the neural network (NN) model has been stored in the folder <b>./model_weights/</b>. This means for instance that the user can start this notebook, run the code cells "load libraries", "create environment", "create agent instance" and then the user can run the testing code in the end of the notebook. Otherwise the notebook is well documented, easy to follow and self-explanatory.   
</div>

#### DDPG agent class
<br>
<div style="text-align: justify">  
The <b>"agent class"</b> is in the file <b>ddpg_agent.py</b>, which is in the <b>root folder of this repository</b>, contains DDPG agent class, with all the elements of the DDPG algorithm excluding the NN models, which are in the file <b>model.py</b> of the same folder. The code in the file is well documented, easy to follow and self-explanatory.   
</div>
  
#### NN model
<br>
<div style="text-align: justify">  
The <b>"fully connected NN model classes"</b> are in the file <b>model.py</b>, which is in the <b>root folder of this repository</b>, containing the fully connected NN model classes, with all the elements of the NN algorithm. The code in the file is well documented, easy to follow and self-explanatory.   
</div>

<h1> Resources and references</h1>
<div style="text-align: justify">  

<br>
Further resources and references regarding this project and DDPG can be found in the following links.
<br>

<ul>
<li><p>Timothy P., et al. "Continuous control with deep reinforcement learning, DDPG (Deep Deterministic Policy Gradients)." <a target="_blank" href="https://arxiv.org/pdf/1509.02971.pdf">https://arxiv.org/pdf/1509.02971.pdf</a> </p>
</li>
<div style="text-align: justify">  
<li><p>John Schulman, et al. "PPO (Proximal Policy Optimization Algorithms)." <a target="_blank" href="https://arxiv.org/pdf/1707.06347.pdf">https://arxiv.org/pdf/1707.06347.pdf</a> </p>
</li>
<li><p>Volodymyr Mnih, et al. "Asynchronous Methods for Deep Reinforcement Learning." <a target="_blank" href="https://arxiv.org/pdf/1602.01783.pdf">https://arxiv.org/pdf/1602.01783.pdf</a> </p>
</li>
<li><p>Gabriel Barth-Maron, et al. "D4PG (Distributed Distributional Deterministic Policy Gradients)." <a target="_blank" href="https://openreview.net/pdf?id=SyZipzbCb">https://openreview.net/pdf?id=SyZipzbCb</a> </p>
</li>
<li><p>Andrej Karpathy. "Andrej Karpathy blog." <a target="_blank" href="http://karpathy.github.io/2016/05/31/rl/">http://karpathy.github.io/2016/05/31/rl/</a></p>
</li>
<li><p>Dhruv Parthasarathy. "Write an AI to win at Pong from scratch with Reinforcement Learning." <a target="_blank" href="https://medium.com/@dhruvp/how-to-write-a-neural-network-to-play-pong-from-scratch-956b57d4f6e0">https://medium.com/@dhruvp/how-to-write-a-neural-network-to-play-pong-from-scratch-956b57d4f6e0</a></p>
</li>
<li><p>Andrej Karpathy, et al. "Evolution Strategies as a Scalable Alternative to Reinforcement Learning." <a target="_blank" href="https://blog.openai.com/evolution-strategies/">https://blog.openai.com/evolution-strategies/</a> </p>
</li>
<li><p>Shixiang Gu, et al. "Q-Prop: Sample-Efficient Policy Gradient with An Off-Policy Critic." <a target="_blank" href="https://arxiv.org/pdf/1611.02247.pdf">https://arxiv.org/pdf/1611.02247.pdf</a> </p>
</li>
<li><p>John Schulman, et al. "High-Dimensional Continuous Control Using Generalized Advantage Estimation." <a target="_blank" href="https://arxiv.org/pdf/1506.02438.pdf">https://arxiv.org/pdf/1506.02438.pdf</a> </p>
</li>
<li><p>Shixiang Gu, et al. "Continuous Deep Q-Learning with Model-based Acceleration, NAF (normalized advantage functions)." <a target="_blank" href="https://arxiv.org/pdf/1603.00748.pdf">https://arxiv.org/pdf/1603.00748.pdf</a> </p>
</li>
<li><p>Udacity, et al. "Deep Reinforcement Learning Nanodegree." <a target="_blank" href="https://github.com/udacity/deep-reinforcement-learning">https://github.com/udacity/deep-reinforcement-learning</a> </p>
</li>
</div>
</ul>
</div>


<hr>
